
FROM ubuntu:22.04
RUN apt-get update && apt-get install -y --no-install-recommends \
        libfontconfig1 libasound2 libx11-6 libxcursor1 libxinerama1 libxrandr2 libxi6 libgl1 \
    && rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY engine.x86_64 ./
RUN chmod +x ./engine.x86_64
EXPOSE 7200/udp
ENTRYPOINT ["./engine.x86_64", "--headless"]

