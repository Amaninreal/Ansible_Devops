# Ansible Playbook for Java and MySQL Installation

This Ansible playbook automates the installation and configuration of Java and MySQL on a local machine. The playbook handles tasks like installing Java, verifying its installation, installing MySQL, starting the MySQL service, securing MySQL, and managing MySQL users.

## Prerequisites

- Ansible 2.x or higher
- Python 3.x (with `mysqlclient` or `PyMySQL` installed)

## Setup

1. Clone the repository or copy the playbook files to your local machine.
2. Ensure you have the required Python dependencies for MySQL by running the following:
   
   ```bash
   pip install mysqlclient

## How to run

1. To run the playbook, use the following command:

    ```bash
    ansible-playbook -i inventory playbooks/main.yml

# Tasks are as follows:

1. **Installs Java (default-jdk)**
   - The playbook installs the default Java Development Kit (default-jdk) using the `apt` module.
   - It ensures that Java is installed on the system to support applications requiring Java.

2. **Verifies the Java Installation**
   - After installing Java, the playbook runs the `java -version` command to confirm that the Java installation was successful.

3. **Installs and Configures MySQL**
   - The playbook installs MySQL using the `apt` module.
   - It ensures that the MySQL service is up and running after installation.

4. **Secures MySQL Installation**
   - The playbook performs a series of actions to secure the MySQL installation:
     - **Sets the MySQL root password** to a specified value.
     - **Removes insecure default users** such as `root@localhost` and `mysql.session@localhost`.
     - **Flushes privileges** to apply changes.

# Example Playbook Execution

    ```bash
    $ ansible-playbook -i inventory playbooks/main.yml


