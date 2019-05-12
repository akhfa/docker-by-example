FROM ubuntu
RUN apt update \
    && apt install -y cmake \
                      git \
                      g++ \
                      libboost-all-dev \
                      libcurl4-openssl-dev \
    && apt clean
RUN git clone https://github.com/akhfa/TebakAngka.git \
    && cd TebakAngka \
    && cmake CMakeLists.txt \
    && make \
    && mv TebakAngka /usr/local/bin/ \
    && cd .. \
    && rm -rf TebakAngka
EXPOSE 18080
ENTRYPOINT [ "TebakAngka", "aaa", "bbb" ]
