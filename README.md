# XL Release Remoting Plugin

### Preface

This document describes the functionality provided by the XL Release Remoting plugin.
For information about XL Release, refer to https://docs.xebialabs.com/xl-release/.

### Overview

The XL Release Remoting Plugin is used to create shared *UnixHost*, *WindowsHost* and *WindowsSshHost*, which can then be leveraged by other plugins for executing the commands on the host. The plugin can also transfer files to the defined host.

As of now, Ansible, Kubernetes and Docker Compose plugins, leverages the XL Release Remoting Plugin. The list of plugins using this shared plugin should go up.

### Features

* Supports SSH for connectivity to Unix and Microsoft Windows.
* Supports CIFS, Telnet, and WinRM for connectivity to Windows hosts.
* Allows SSH jumpstations to be used to access hosts to which a direct network connection is not possible.
  *Note*: In addition to SSH connections, CIFS, Telnet, and WinRM connections can be tunneled through an SSH jumpstation.

### Usage

We need to define the required hosts under Configuration tab in XL Release.

#### Supported Host Types

* Unix Host
* Windows SSH Host
* Windows Host

#### Properties:

| Property | Description |
| -------- | ----------- |
| Title | Any title for the remote host |
| Address | Remote host IP address |
| Port | Remote host Port number |
| Username | User ID to use when connecting to the host |
| Password | Password to use when connecting to the host |
| Private Key File | Private key file to use for authentication (*SSH host only*) |
| Passphrase | Passphrase for the private key in the private key file (*SSH host only*) |
| SUDO username | Username to sudo to when accessing files or executing commands |
| SU username | Username to su to when accessing files or executing commands |
| SU password | Password of user to su to when accessing files or executing commands |
| connectionType | Type of connection to create. Eg SUDO, SFTP, SFTP_WINSSHD, TELNET, WINRM_INTERNAL etc. |
