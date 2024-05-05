FROM ubuntu

RUN apt update \
    && apt install -y ffmpeg python3 python3-pip python3-venv \
    && apt clean

RUN python3 -m venv /venv
ENV PATH="/venv/bin:$PATH"

RUN pip install -U openai-whisper
RUN pip install setuptools-rust

ENTRYPOINT [ "bash" ]
