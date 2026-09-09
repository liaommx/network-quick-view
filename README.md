# Network Quick View

A lightweight, single-file HTML tool for managing and visualizing network devices, nodes, subnets, IP addresses, and DHCP relationships.

No server or installation is required. Open `network_quick_view.html` directly in a web browser.

## Features

- Organize devices by location, network node, device, and multiple IP addresses
- Device roles: Router / Gateway, Peer Relay, VPN Server, DHCP Server
- Custom subnet names and colors
- CIDR-based automatic IP/subnet matching
- Longest Prefix Match for overlapping networks
- DHCP subnet assignment
- Add, edit, and delete devices and subnets
- Quickly rename locations and node names
- Load and save configuration files
- Export a static read-only HTML snapshot

## Data Handling

The main HTML file does not contain real network configuration.

Every time `network_quick_view.html` is opened or refreshed, it starts with anonymized example data. Actual network data must be loaded manually from a configuration TXT file.

Configuration data is not automatically restored from browser LocalStorage. The TXT configuration file is intended to be the persistent source of truth for actual network information.

## Configuration Workflow

1. Open `network_quick_view.html`.
2. Click **載入設定** and select your configuration TXT file.
3. Edit or review the network topology.
4. Click **儲存設定** to save the updated configuration.

The configuration format is kept compatible with the existing Network Quick View TXT format.

## Static Export

The tool can export the currently loaded topology as a standalone, read-only HTML page.

Unlike the main application HTML, a static export may contain real network information. Treat exported files accordingly.

## Usage

Clone the repository:

```bash
git clone https://github.com/liaommx/network-quick-view.git
cd network-quick-view
```

Then open `network_quick_view.html` in a web browser.

No build process, package manager, web server, or external dependencies are required.

## Version History

Development history is maintained using Git commits and tags, starting from `v6.1`.

To inspect a specific version:

```bash
git checkout v6.10
```

To return to the latest development version:

```bash
git checkout main
```

## Privacy / Security

Do not commit configuration TXT files containing real network information to a public repository.

The repository version of `network_quick_view.html` should contain anonymized example data only.

If configuration files are stored inside the repository directory, consider adding the following to `.gitignore`:

```gitignore
*.txt
```

## License

No license has been specified yet.
