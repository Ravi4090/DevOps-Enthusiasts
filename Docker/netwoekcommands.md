Here are some Docker network-related commands along with brief explanations:

1. **docker network create**:
   - Creates a new Docker network.
   - Syntax: `docker network create [OPTIONS] NETWORK`
   - Example: `docker network create my_network`

2. **docker network ls**:
   - Lists all Docker networks present on the system.
   - Syntax: `docker network ls [OPTIONS]`
   - Example: `docker network ls`

3. **docker network inspect**:
   - Provides detailed information about a specific Docker network.
   - Syntax: `docker network inspect [OPTIONS] NETWORK [NETWORK...]`
   - Example: `docker network inspect my_network`

4. **docker network rm**:
   - Deletes one or more Docker networks.
   - Syntax: `docker network rm [OPTIONS] NETWORK [NETWORK...]`
   - Example: `docker network rm my_network`

5. **docker network prune**:
   - Deletes all unused Docker networks.
   - Syntax: `docker network prune [OPTIONS]`
   - Example: `docker network prune`

6. **docker network connect**:
   - Connects a Docker container to an existing network.
   - Syntax: `docker network connect [OPTIONS] NETWORK CONTAINER`
   - Example: `docker network connect my_network my_container`

7. **docker network disconnect**:
   - Disconnects a Docker container from a network.
   - Syntax: `docker network disconnect [OPTIONS] NETWORK CONTAINER`
   - Example: `docker network disconnect my_network my_container`

8. **docker run --network**:
   - Specifies the network for a newly created container.
   - Syntax: `docker run [OPTIONS] --network NETWORK IMAGE [COMMAND] [ARG...]`
   - Example: `docker run --network=my_network my_image`

These commands allow users to manage Docker networks effectively, including creating, listing, inspecting, updating, and removing networks. Additionally, they provide options for connecting and disconnecting containers from networks, as well as specifying the network for newly created containers.