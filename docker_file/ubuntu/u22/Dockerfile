FROM ubuntu:22.04

ARG DEBIAN_FRONTEND=noninteractive

ENV TZ Asia/Seoul
ENV PYTHONIOENCODING UTF-8
ENV LC_CTYPE C.UTF-8

WORKDIR /root

RUN apt update && apt install -y netcat
RUN apt install vim git gcc ssh curl wget gdb sudo zsh python3 python3-pip libffi-dev build-essential libssl-dev libc6-i386 libc6-dbg gcc-multilib make -y

RUN dpkg --add-architecture i386
RUN apt update
RUN apt install libc6:i386 -y

RUN python3 -m pip install --upgrade pip

RUN wget https://github.com/Significant-Gravitas/Auto-GPT/archive/refs/tags/v0.4.3.tar.gz
RUN tar -xzvf *.tar.gz
RUN cd Auto-GPT-0.4.3
RUN cd Auto-GPT-0.4.3
RUN ls
RUN pip3 install update

RUN python3 -c 'print("OPENAI_API_KEY=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")' > .env
RUN python3 -c 'print("PINECONE_API_KEY=9ab71be0-1e76-457c-8d49-b38f502e0c9f")' >> .env
RUN python3 -c 'print("PINECONE_ENV=northamerica-northeast1-gcpf")' >> .env
RUN python3 -c 'print("SMART_LLM_MODEL=gpt-3.5-turbo")' >> .env
RUN python3 -c 'print("FAST_LLM_MODEL=gpt-3.5-turbo")' >> .env
RUN python3 -c 'print("HUGGINGFACE_AUDIO_TO_TEXT_MODEL=CompVis/stable-diffusion-v1-4")' >> .env
RUN python3 -c 'print ("GOOGLE_API_KEY=AIzaSyCBTWaBvnQ6EqRLvkNPjt__fwMv-DjEKxY")' >> .env
RUN python3 -c 'print ("GOOGLE_CUSTOM_SEARCH_ENGINE_ID=b7d67a59cf950471b")' >> .env


