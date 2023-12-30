# Use the official Ubuntu image with XFCE desktop
FROM ubuntu:20.04

# Install necessary packages
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    xfce4 \
    xfce4-terminal \
    firefox

# Set the default user and its password (change as needed)
RUN useradd -ms /bin/bash user
RUN echo "user:user" | chpasswd

# Set the display environment variable
ENV DISPLAY=:1

# Start the XFCE desktop on container launch
CMD ["startxfce4"]
