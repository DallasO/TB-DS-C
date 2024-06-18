# FROM pypy:3.9-slim-bookworm
FROM python:3-alpine3.11

# mac
## brew
### brew install git-lfs openblas
### git lfs install
### 

WORKDIR /usr/src/app
# RUN apt-get update
# RUN apt-get upgrade -y
# RUN apt install -y build-essential gfortran cmake libopenblas-dev pkg-config
RUN apk update
# subversion openblas
RUN apk add --update make automake cmake gcc g++ python3-dev gfortran build-base py3-scipy openblas-dev
RUN python -m pip install --upgrade pip 

# RUN pip install scipy==1.10.1 --only-binary numpy

COPY requirement.txt ./
RUN pip install --no-cache-dir -r requirement.txt

COPY . .

CMD ["python", "app.py"]
