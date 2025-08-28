FROM pytorch/pytorch:1.7.1-cuda11.0-cudnn8-runtime


ENV DEBIAN_FRONTEND=noninteractive


RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    wget \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get update && apt-get install -y nvidia-utils-470

WORKDIR /workspace


COPY requirements.txt .


RUN pip install --no-cache-dir -r requirements.txt


VOLUME /workspace/sandbox

CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
#CMD ["bash"]
