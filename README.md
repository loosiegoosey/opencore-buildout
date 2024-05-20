# OpenCore Buildout

## Overview
OpenCore Buildout is a comprehensive buildout configuration for setting up multiple versions of the Plone CMS (Content Management System). This project facilitates the setup and maintenance of Plone environments for versions 3.2, 3.3, and 4.x, leveraging Buildout, a powerful build system for creating, assembling and deploying applications.

## Features
- Supports Plone versions 3.2, 3.3, and 4.x
- Provides automated setup scripts
- Utilizes Zope Public License (ZPL) for code distribution
- Easy to extend and customize for additional configurations
- Comprehensive dependency management

## Installation Instructions

### Prerequisites
- Python installed on your system (recommended version: 2.7)
- `virtualenv` for isolated Python environments
- Access to the GitHub repository

### Steps to Install
1. **Clone the Repository**
   ```sh
   git clone https://github.com/Yuriy/opencore-buildout.git
   cd opencore-buildout
   ```

2. **Create a Virtual Environment**
   ```sh
   virtualenv venv
   source venv/bin/activate
   ```

3. **Bootstrap the Buildout**
   - For Plone 3.2
     ```sh
     python plone-3.2/bootstrap.py
     ```
   - For Plone 3.3
     ```sh
     python plone-3.3/bootstrap.py
     ```
   - For Plone 4
     ```sh
     python plone-4/bootstrap.py
     ```

4. **Run Buildout**
   ```sh
   bin/buildout
   ```

5. **Start the Plone Instance**
   ```sh
   bin/instance fg
   ```

## Usage Examples
Once installed, you can start the Plone instance and use it as per your requirements. Here’s a basic example of how you might interact with the Plone CMS:

### Starting the Instance
```sh
bin/instance start
```

### Stopping the Instance
```sh
bin/instance stop
```

### Accessing Plone in Your Browser
Navigate to `http://localhost:8080` to access the Plone web interface.

## Code Summary

### Directory Structure
The project is divided into sub-directories each representing a version of Plone:
- `plone-3.2/` - Contains the buildout configuration and bootstrap script for Plone 3.2.
- `plone-3.3/` - Contains the buildout configuration and bootstrap script for Plone 3.3.
- `plone-4/` - Contains the buildout configuration and bootstrap script for Plone 4.

### Key Files
- `bootstrap.py`: This script sets up the initial configuration required to run a Buildout for the specific Plone version. Each `bootstrap.py` in their respective directories is responsible for bootstrapping that version of Plone.

### Notable Content in `bootstrap.py`
```python
##############################################################################
#
# Copyright (c) 2006 Zope Corporation and Contributors.
# All Rights Reserved.
#
# This software is subject to the provisions of the Zope Public License,
# Version 2.1 (ZPL).  A copy of the ZPL should accompany this distribution.
# THIS SOFTWARE IS PROVIDED "AS IS" AND ANY AND ALL EXPRESS OR IMPLIED
# WARRANTIES ARE DISCLAIMED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
# WARRANTIES OF TITLE, MERCHANTABILITY, AGAINS
```
This content indicates that the scripts are licensed under the Zope Public License (ZPL) Version 2.1 and carries disclaimers regarding warranties.

## Contributing Guidelines
We welcome contributions from the community. To contribute:

1. Fork the repository on GitHub.
2. Create a new branch from the main branch (`main` or `master`).
3. Make your changes and commit them with clear commit messages.
4. Push your changes to your forked repository.
5. Open a Pull Request (PR) against the main repository.
6. Ensure that your code passes any existing tests and adheres to the coding standards.

Please review the project’s contribution guidelines and Code of Conduct before submitting your contributions.

## License
This project is licensed under the Zope Public License (ZPL), Version 2.1. You can find a copy of the license in the repository.

---

This README provides a comprehensive overview and should help you get started with the OpenCore Buildout project. For more detailed documentation, please refer to the official Plone and Buildout documentation.