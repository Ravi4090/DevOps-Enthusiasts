## Module 2: Central vs Distributed Version Control System

### 1. **Distributed Version Control System (DVCS):**

- **Definition:**
  - In a DVCS, each user has a complete copy of the entire repository, including its history, on their local machine.
  
- **Working Mechanism:**
  - Developers can work independently, having their own local branches and making commits without needing a constant connection to a central server.

- **Flexibility:**
  - Enables offline work and supports parallel development through branching, merging, and creating isolated environments.

- **Example:**
  - Git is a prominent example of a distributed version control system.

### 2. **Centralized Version Control System (CVCS):**

- **Definition:**
  - In a CVCS, there is a central server that stores the entire version history. Developers check out a working copy from this central repository.

- **Working Mechanism:**
  - Developers commit changes to the central repository, and updates are pulled from and pushed to this central location.

- **Dependency on Central Server:**
  - Requires a constant network connection to the central server for most operations.

- **Example:**
  - Subversion (SVN) is a well-known centralized version control system.

### Comparison:

| **Aspect**                  | **Distributed VCS (DVCS)**                  | **Centralized VCS (CVCS)**                    |
|-----------------------------|--------------------------------------------|-----------------------------------------------|
| **Local Repository**         | Each user has a complete copy locally.     | Developers have a working copy linked to the central repository.                   |
| **Independence**            | Developers can work independently.         | Developers are dependent on the central server for most operations.                    |
| **Offline Work**             | Possible – developers can work offline.    | Requires a constant network connection.        |
| **Branching and Merging**    | Efficient and supports parallel development. | Branching and merging can be more centralized and may involve more coordination. |
| **Example**                  | Git                                        | Subversion (SVN)                              |
