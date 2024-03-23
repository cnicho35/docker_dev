# Use a base image with a C++ compiler installed
FROM gcc:latest

RUN apt-get update && apt-get install -y cmake

# Set the working directory inside the container
WORKDIR /app

# Copy the source code into the container
COPY src/hello_world.cpp ./src/hello_world.cpp
COPY CMakeLists.txt .

# Compile the C++ program using CMake
RUN mkdir build/ && cd build && cmake .. && make

# Specify the command to run when the container starts
CMD ["./build/hello_world"]
# Specify the command to run when the container starts
