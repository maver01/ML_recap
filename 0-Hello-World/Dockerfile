# Comments created by MS in 2023.12.17
# define the python version
FROM python:3.9

# define the location of the working directory (/app as it is already in the location)
WORKDIR /app

# copy the poetry files into the work directory
COPY pyproject.toml poetry.lock ./

# install poetry from pip, install the libraries using poetry install
RUN pip install poetry && \
    poetry config virtualenvs.create false && \
    poetry install --no-dev --no-interaction --no-ansi

# copy everything in the working directory into the new directory
COPY . .

# Execute python main.py
CMD ["python", "./src/main.py"]

