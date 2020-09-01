# FROM ubuntu:18.04
# RUN apt-get update && \
#     apt-get install -y \
#         python \
#         curl \
#         net-tools \
#         pgp \
#         xz-utils \
#         unzip \
#         libicu60 \
#         libmpc3 \
#         libfl2 && \
#     rm -rf /var/lib/apt/lists/*
# RUN curl -L -O https://github.com/Kitware/CMake/releases/download/v3.14.5/cmake-3.14.5-Linux-x86_64.tar.gz && \
#     tar -xf cmake-3.14.5-Linux-x86_64.tar.gz && \
#     rm cmake-3.14.5-Linux-x86_64.tar.gz
# RUN curl -L -O https://github.com/ninja-build/ninja/releases/download/v1.9.0/ninja-linux.zip && \
#     unzip ninja-linux.zip && \
#     rm ninja-linux.zip
# RUN curl -L -o install_azure_sphere_sdk.sh https://aka.ms/AzureSphereSDKInstall/Linux && \
#     chmod +x /install_azure_sphere_sdk.sh && \
#     mkdir -p /etc/udev/rules.d && \
#     yes | /install_azure_sphere_sdk.sh && \
#     rm install_azure_sphere_sdk.sh
# RUN curl -L -O https://developer.arm.com/-/media/Files/downloads/gnu-rm/9-2019q4/gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2 && \
#     tar -xf gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2 && \
#     rm gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2;
# ENV PATH "$PATH:/:/cmake-3.14.5-Linux-x86_64/bin:/gcc-arm-none-eabi-9-2019-q4-major/bin"

FROM mcr.microsoft.com/azurespheresdk:latest
RUN curl -L -O https://developer.arm.com/-/media/Files/downloads/gnu-rm/9-2019q4/gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2 && \
    tar -xf gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2 && \
    rm gcc-arm-none-eabi-9-2019-q4-major-x86_64-linux.tar.bz2;
ENV PATH "$PATH:/:/gcc-arm-none-eabi-9-2019-q4-major/bin"
