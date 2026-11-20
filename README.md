# ns8-pegaprox

[PegaProx](https://pegaprox.com) is a multi-cluster management solution for Proxmox VE.

## Install

Install from the Software Center: in cluster-admin, add a software repository
named `dz00te` with URL `https://forge.dzlab.net/ns8/updates/` (see the
[repository website](https://forge.dzlab.net/) for instructions), then install
PegaProx from the Software Center.

Install from CLI, replacing `<version>` with the
[latest release](https://github.com/dz00te/ns8-pegaprox/releases/latest)
(e.g. `0.2.1`) and `1` with the ID of the target node:

    add-module ghcr.io/dz00te/pegaprox:<version> 1

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
