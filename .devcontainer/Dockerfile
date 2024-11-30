FROM pytorch/pytorch:latest

RUN sudo apt-get update && apt-get install -y \
    python3-pip \
    && sudo rm -rf /var/lib/apt/lists/*

RUN pip install torch torchvision torchaudio

RUN pip install transformers

WORKDIR /app

COPY . /app

CMD [ "python", "start.py"]