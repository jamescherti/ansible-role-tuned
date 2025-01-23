# ansible-role-tuned
![License](https://img.shields.io/github/license/jamescherti/ansible-role-tuned)

This Ansible playbook manages the installation, configuration, and activation of the tuned service.

Tuned is a dynamic adaptive system tuning tool used in Linux environments to optimize performance by adjusting various system settings dynamically. It provides pre-defined profiles that target specific use cases, such as high throughput, low latency, and energy saving, and automatically applies these configurations based on system activity.

For high traffic servers, using Tuned is beneficial as it can enhance network throughput and responsiveness by adjusting parameters like CPU frequency scaling, I/O scheduling, and network stack settings. This optimization results in improved server performance, reduced latency, and better handling of high loads, ultimately leading to a more efficient and reliable infrastructure for handling significant network traffic.

## Features

- Install tuned and configure it using the Ansible variables: `tuned_daemon`, `tuned_dynamic_tuning`, `tuned_sleep_interval`, `tuned_update_interval`, and `tuned_recommend_command`.
- Activate the specified tuned profile using the `tuned_profile` variable. (When the `tuned_profile` is not set, the role installs only tuned.)
- Supports Debian/Ubuntu and RedHat family based operating systems.

## Usage

### Example Playbook

Here is an example of how to use ansible-role-tuned after installing it in the `roles/tuned` directory:

```yaml
- hosts: SERVER
  roles:
    - {role: tuned,
       tuned_profile: "throughput-performance"}
```

## Author and license

Copyright (C) 2020-2025 [James Cherti](https://www.jamescherti.com).

Distributed under terms of the MIT license.

# Links

- [ansible-role-tuned @GitHub](https://github.com/jamescherti/ansible-role-tuned)
