# Ansible Setup

This repo contains Ansible playbooks and roles to set up environments for **Arch Linux** and **MacOS** machines.

---

## Clone the repo

Clone the repo into your `~/personal` directory (or wherever you like):

```bash
mkdir -p ~/personal
cd ~/personal
git clone https://github.com/LuckyBastrd/ansible.git
cd ansible
```

---

## Usage

The main entry point is the `run` script. It installs required roles/collections and runs the appropriate playbook.

### Run for Arch Linux

```bash
./run arch
```

This will:

- Install dependencies listed in `requirements-arch.yml`
- Run the Arch setup playbook `arch/setup-arch.yml`

### Run for MacOS (not yet)

```bash
./run mac
```

This will:

- Install dependencies listed in `requirements-mac.yml`
- Run the MacOS setup playbook `mac/setup-mac.yml`

---

## Notes

- The `run` script will prompt for your sudo password when needed.
- Ansible roles and collections are installed automatically before running playbooks.
- The repo uses separate `ansible.cfg` files in each environment folder for clear role paths.

---

## Requirements

- Ansible installed (recommend latest stable version)
- SSH access configured if you run playbooks on remote hosts (optional; current playbooks use `connection: local`)
