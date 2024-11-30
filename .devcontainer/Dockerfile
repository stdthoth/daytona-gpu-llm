FROM pytorch/pytorch:latest

RUN apt-get update && apt-get install -y \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN pip install torch torchvision torchaudio

RUN pip install transformers

WORKDIR /app

COPY . /app

CMD [ "python", "start.py"]