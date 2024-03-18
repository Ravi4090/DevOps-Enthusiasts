
# Docker Image Management Commands

An image in Docker is a lightweight, standalone, executable package that contains everything needed to run a piece of software, including the code, runtime, libraries, dependencies, and environment variables. It serves as a blueprint for creating containers, which are instances of images that run in isolated environments.

## Key Docker Commands for Images

1. **docker images**: Lists all the images available on the local machine.
   ```bash
   docker images
   ```

2. **docker pull**: Downloads an image from a registry (e.g., Docker Hub) to the local machine.
   ```bash
   docker pull <image_name>
   ```

3. **docker push**: Uploads an image from the local machine to a registry (e.g., Docker Hub).
   ```bash
   docker push <image_name>
   ```

4. **docker build**: Builds a Docker image from a Dockerfile.
   ```bash
   docker build -t <image_name> <path_to_Dockerfile>
   ```

5. **docker rmi**: Removes one or more images from the local machine.
   ```bash
   docker rmi <image_name or image_id>
   ```

6. **docker tag**: Tags an image with a new name and/or tag.
   ```bash
   docker tag <source_image>[:tag] <target_image>[:tag]
   ```

7. **docker inspect**: Displays detailed information about an image, including its configuration and metadata.
   ```bash
   docker inspect <image_name or image_id>
   ```

8. **docker history**: Displays the history of an image, showing the intermediate layers and commands used to create it.
   ```bash
   docker history <image_name or image_id>
   ```

9. **docker save**: Saves one or more images to a tar archive file.
   ```bash
   docker save -o <output_file.tar> <image_name>
   ```

10. **docker load**: Loads images from a tar archive file created with docker save.
    ```bash
    docker load -i <input_file.tar>
    ```

11. **docker commit**: Creates a new image from a container's changes.
    ```bash
    docker commit <container_id> <new_image_name>
    ```

12. **docker import**: Imports the contents of a tar archive as a new filesystem image.
    ```bash
    docker import <file_path> <image_name>
    ```

These commands allow you to interact with Docker images, including listing, pulling, pushing, building, tagging, inspecting, and managing images on your local machine or a Docker registry. They are essential for managing the lifecycle of Docker images, from creation to distribution and deployment.
