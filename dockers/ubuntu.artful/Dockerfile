FROM ubuntu:artful
MAINTAINER developers@moneymanagerex.org
ADD https://repos.codelite.org/CodeLite.asc /etc/apt/trusted.gpg.d/
RUN chown _apt:root /etc/apt/trusted.gpg.d/CodeLite.asc && \
    echo 'deb http://repos.codelite.org/wx3.1/ubuntu/ artful universe' \
      >/etc/apt/sources.list.d/CodeLite.list && \
    apt-get update && \
    apt-get install -y --no-install-recommends \
      cmake build-essential gettext git pkg-config lsb-release file ccache \
      libwxgtk-webview3.1-dev liblua5.3-dev libcurl4-openssl-dev && \
    apt-get clean

ENV MMEX_INST_CMD apt install -yqV ./mmex_*.deb
