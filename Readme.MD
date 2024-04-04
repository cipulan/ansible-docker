**Ansible Playbook README**

**Description:**

This Ansible playbook automates the installation Docker Engine and Docker Compose

**Roles:**

1. **Pre-Check:**

   - Verifies the availability of the required packages and dependencies for Docker Engine and Docker Compose.
   - Checks the status of the Docker service to ensure it is not already running.
   - Exits the playbook if the prerequisites are not met or the Docker service is already active.

2. **common:**

   - Installs the required packages and dependencies for Docker Engine and Docker Compose.
   - Configures the Docker repository and installs the Docker Engine and Docker Compose packages.
   - Enables and starts the Docker service to ensure it is running correctly.

3. **repository:**

   - Sets up the Docker repository to install the latest version of Docker Engine and Docker Compose.
   - Adds the Docker GPG key and configures the repository to fetch the latest packages.
   - Updates the package cache and installs the Docker Engine and Docker Compose packages.

4. **docker:**

   - Installs the Docker Engine and Docker Compose packages using the package manager.
   - Configures the Docker service to start on boot and enables it to run as a system service.
   - Starts the Docker service to ensure it is running correctly.

5. **post-install:**

   - Verifies the installation of Docker Engine and Docker Compose by checking the version of the installed packages.
   - Displays a message confirming the successful installation of Docker Engine and Docker Compose.
   - Sends a notification to a Telegram chat group using a custom bash script to alert the user about the successful installation.

   **Usage:**

6. Ensure Ansible is installed on the control node.
7. Change hosts file with the IP address of the target host.
8. Test Host with the following command: `ansible all -m ping` or `ansible-playbook ping.yml`.
9. Run the playbook using the command: `ansible-playbook main.yml`.

**Note:**

- Test the playbook thoroughly in a controlled environment before deploying to production to avoid unexpected behavior.
- Regularly review and update the playbook to incorporate any changes or improvements in your environment or requirements.

**Author:**

[cipulan]

**Contact:**

[https://github.com/cipulan]

**License:**

[Docker Engine overview]
[https://docs.docker.com/engine/]
