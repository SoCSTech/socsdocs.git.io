# How to use Docker and Dev Containers for Labs and Workshops

We use **Dev Containers** to provide a consistent configuration for **Visual Studio Code** on our Lab PCs running Windows.

Dev Containers work by opening a **Docker container** in the background, and running everything inside it. Docker containers run Linux (and on Windows that’s being done with the **WSL2 sub-system**).

### **Why Use Dev Containers?**

*   Provides a consistent development environment across lab PCs.
*   Allows easy replication of the lab setup on personal devices.
*   Supports Linux-based compute libraries that may not run natively on Windows.

To replicate the lab environment on your own computer, find and clone the module repository from [**github.com/socstech**](https://github.com/socstech) or [**github.com/uol-socs**](https://github.com/uol-socs)

And then ensure you have the following dependencies installed:

*   **[Git](https://git-scm.com/)**
*   **[Docker](https://docs.docker.com/get-started/get-docker/)**
*   **[Visual Studio Code](https://code.visualstudio.com/)**
    *   **[Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)**

Some modules also use standalone Docker containers. Some are pre-running inside **Docker Desktop** on the lab PCs, while others have specific instructions provided in the module’s **Blackboard site**.

- - -

## **Using Dev Containers on Windows**

1.  **Log into the lab computers.** If you don’t know the password, ask a member of the teaching staff.
2.  **Open the ‘Docker Containers’ folder** on the desktop.
3.  **Choose your subject area:**
    *   _Computer Science & Robotics_
    *   _Maths & Physics_
4.  **Select your workspace**, typically named after the module code and title. Double-click the icon to launch it.
5.  **Open the terminal**:
    *   Click **‘Terminal > New Terminal’** at the top.
    *   OR use the shortcut **Ctrl + Shift + \`**
6.  **Update your container configuration:**
    *   Run: `git pull`
    *   If you see **‘Already up to date’**, proceed.
        *   But, If you see a message like **‘Your local changes to the following file will be overwritten by merge’**, delete the affected files in VS Code’s file explorer and try again.
7.  **Reopen the container**:
    *   Press **F1** or **Ctrl + Shift + P**.
    *   Type **‘Reopen in Container’** and press **Enter**.
8.  **If you get a Docker error (‘Daemon is not running’):**
    *   Open **Docker Desktop** and let it fully launch before trying again.
9.  **Once the container is running**, you’ll see the module/container name in the **bottom-left corner** of VS Code. You’re now ready to use it!

## **Using Standalone Docker Containers on Windows**

Some containers, such as **MySQL** and **PostgreSQL**, are shared between multiple modules but run in the background.

1.  **Open Docker Desktop** (from the taskbar or Start menu).
2.  **Wait for Docker Desktop to fully launch**.
3.  **Open the ‘Containers’ tab** in the sidebar.
4.  **Start a container**:
    *   Click the **Play/Start** button next to the desired container.
5.  **If you’re using database containers, we have provided some admin interfaces:**
    *   **MySQL**: Use **PhpMyAdmin** as an admin interface.
    *   **PostgreSQL**: Use **PGAdmin** for management.
6.  **Verify the container is running**:
    *   A **green icon** will appear next to the container.
    *   The forwarded **ports** will be accessible from your local machine.

- - -

## **Using Docker on Linux**

On Linux, we use the **Docker Engine** instead of **Docker Desktop**. The main differences are:

*   **No graphical interface**: Containers must be managed entirely through the terminal.
*   **Container storage location**: Pre-distributed containers are stored in the **Documents** folder rather than a dedicated Docker folder.
*   **Checking container status**: Use `docker ps` to list running containers and `docker ps -a` to see all containers.
*   **Stopping containers**: Use `docker stop <container_name>`.
*   **Removing containers**: Use `docker rm <container_name>`.
*   **Logs and debugging**: Use `docker logs <container_name>` to view container logs.

Follow the same steps as Windows for launching Dev Containers, but all interactions must be performed via the terminal.

- - -

## **FAQs**

### **Why do I have to use Docker?**

*   Ensures dependencies between teaching modules do not conflict.
*   Allows technicians and academics to provide updates without disrupting lab access.

### **Docker has crashed on Windows**

If Docker crashes, Windows may have closed unused applications to save power, if you’re not using Docker — you can ignore this.

However, if you’re trying to use this, you should try to do the following:

1.  If prompted, Restart the Ubuntu WSL integration.
2.  Restart Docker Desktop, by right-clicking on the Docker icon in the bottom right and clicking ‘Restart’.
3.  Wait until Docker has fully launched before trying to make use of it.

If this doesn’t resolve your issues, **Report the problem via ‘Report a Tech Issue’** (desktop link or QR code on your desk), and then **Move to another lab computer**.

### **How can I create my own Dev Container?**

If you have never used Docker before, we recommend watching [Docker Tutorial for Beginners by Programming with Mosh](https://youtu.be/pTFZFxd4hOI) to gain some background knowledge.

To create your own Dev Container, follow the official documentation from **Visual Studio Code**. It provides step-by-step instructions on setting up a custom container. Refer to the guide here: [Create a Dev Container (VS Code Docs)](https://code.visualstudio.com/docs/devcontainers/create-dev-container).

If you require any assistance with creating containers, please [Contact Us](https://socstech.support/contact-us/).