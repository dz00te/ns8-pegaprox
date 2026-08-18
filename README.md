# ns8-pegaprox

[PegaProx](https://pegaprox.com) is a multi-cluster management solution for Proxmox VE.

## Install

Install via Software center:
  - Add a Software repository pointing to `https://forge.dzlab.net/ns8/updates/`, check out the [repository website](https://forge.dzlab.net/) for instructions.

Install from CLI:

    add-module ghcr.io/dz00te/pegaprox:0.0.13

## Configure

Set the FQDN in the module settings and browse to it.

For default credentials and usage, see the [PegaProx Documentation](https://docs.pegaprox.com/).

## Uninstall

To uninstall the instance:

    remove-module --no-preserve pegaprox1

## Debug

Enter the module environment:

    runagent -m pegaprox1

Check services and logs:

    systemctl --user status pegaprox.service
    podman logs pegaprox-app

## Documentation

- [PegaProx Documentation](https://docs.pegaprox.com/)
- [PegaProx GitHub](https://github.com/PegaProx/project-pegaprox)