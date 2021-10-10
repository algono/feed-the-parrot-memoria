FROM archlinux

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Create non-root user
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

# Install LaTeX
RUN pacman -Sy --noconfirm --needed git make pandoc texlive-most 

# [Optional] Set the default user. Omit if you want to keep the default as root.
USER $USERNAME
