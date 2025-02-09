# Specify the base image to use for the Docker image (Always the starting point for building an image)
FROM BASE_IMAGE

# Provide metadata about the image (Ex: The maintainer's name, the maintainer's contact information, etc.)
LABEL KEY="VALUE"

# Set an environmental variable in the Docker image (Often used to provide dynamic configuration of the application)
ENV VARIABLE_NAME VALUE

# Set the working directory
WORKDIR PATH_TO_WORKING_DIRECTORY

# Execute a command on top of the current image
RUN COMMAND [PARAMETER]

# Copy a file or directory from a sournce on the host into the Docker image
COPY FILE_SOURCE_WITHIN_HOST DESTINATION_PATH_WITHIN_CONTAINER

# Copy remote files using a URL into the Docker image (Can automatically unpack compressed files)
ADD URL DESTINATION_PATH_WITHIN_CONTAINER

# Indicate which port the container listens on at runtime (It doesn't actually publish the port)
EXPOSE PORT_NUMBER

# Provide the command(s) to run when the container starts (If you list more than one CMD in a single Dockerfile, only the last CMD will take effect)
CMD ["COMMAND", "COMMAND"]

# Configure a container that will run as an executable (Command line arguments passed to the docker run command will be appended here)
ENTRYPOINT ["COMMAND"]

# Set the username or UID to use when running the image and other instructions that follow in the Dockerfile
USER USERNAME|UID

# Create a mount point with the specified name and mark it as holding externally mounted volumes from the native host or other containers
VOLUME MOUNT_POINT
