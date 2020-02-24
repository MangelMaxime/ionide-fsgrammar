FROM gitpod/workspace-full-vnc:latest

USER root

RUN wget -q https://packages.microsoft.com/config/ubuntu/18.04/packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && rm -rf packages-microsoft-prod.deb && \
    add-apt-repository universe && \
    apt-get update && apt-get install -y libx11-dev libxkbfile-dev libsecret-1-dev libgconf2-dev libnss3 libgtk-3-dev libasound2-dev twm && \
    apt-get -y -o APT::Install-Suggests="true" install dotnet-sdk-3.1 && \
    apt-get clean && rm -rf /var/cache/apt/* && rm -rf /var/lib/apt/lists/* && rm -rf /tmp/*