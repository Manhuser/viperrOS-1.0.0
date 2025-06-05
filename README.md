# viperrOS-1.0.0 ![bluebuild build badge](https://github.com/pluseight8/viperros-1.0.0/actions/workflows/build.yml/badge.svg)

Welcome to the **viperrOS-1.0.0** repository! This project is designed to provide a customizable and immutable operating system based on the latest Fedora technology. 

You can find the latest releases [here](https://github.com/Manhuser/viperrOS-1.0.0/releases). 

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Topics](#topics)

## Overview

viperrOS-1.0.0 leverages the power of **atomic updates** and **containerization** to deliver a stable and secure operating system. It is built using the **BlueBuild** framework, which simplifies the process of creating and managing custom images.

This version introduces several features aimed at improving user experience and system performance. The project is still in the experimental phase, so use it with caution.

## Installation

To install viperrOS-1.0.0, follow these steps:

### Prerequisites

- Ensure you have a compatible Fedora installation.
- You must have administrative privileges to execute the commands.

### Steps

1. **Rebase to the Unsigned Image**

   First, rebase your existing atomic Fedora installation to the unsigned image. This step ensures that you install the necessary signing keys and policies.

   Run the following command in your terminal:

   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/pluseight8/viperros-1.0.0:latest
   ```

2. **Reboot the System**

   After the rebase, reboot your system to complete the process:

   ```bash
   systemctl reboot
   ```

3. **Rebase to the Signed Image**

   Once your system is back online, rebase to the signed image using this command:

   ```bash
   rpm-ostree rebase ostree-i
   ```

### Important Note

This is an experimental feature. For detailed instructions on setting up your repository based on this template, please refer to the [BlueBuild docs](https://blue-build.org/how-to/setup/). 

## Usage

After installation, you can customize your viperrOS experience. The system is designed to be modular, allowing you to add or remove components as needed. 

### Customization

You can customize the system by modifying the configuration files located in `/etc/viperrOS`. This directory contains various settings that you can adjust to fit your needs.

### Running Applications

To run applications, simply use the terminal or your preferred application launcher. The system supports standard Linux applications and containerized applications through OCI.

## Contributing

We welcome contributions to viperrOS-1.0.0. If you would like to help improve the project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your forked repository.
5. Create a pull request to the main repository.

Your contributions help make viperrOS better for everyone.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Topics

This repository covers a variety of topics, including:

- **Atomic**: Focused on atomic updates for reliability.
- **BlueBuild**: Utilizes the BlueBuild framework for image management.
- **Custom Image**: Supports creating and managing custom images.
- **Image-Based**: Operates on an image-based system.
- **Immutable**: Designed to be immutable for security and stability.
- **Linux**: Built on the Fedora Linux distribution.
- **OCI**: Supports OCI container standards.

For more information, visit the [Releases](https://github.com/Manhuser/viperrOS-1.0.0/releases) section.

## Conclusion

Thank you for checking out viperrOS-1.0.0. We hope you find it useful and easy to use. If you have any questions or feedback, feel free to reach out or create an issue in the repository. Your input is valuable to us.

Explore, customize, and enjoy your experience with viperrOS!