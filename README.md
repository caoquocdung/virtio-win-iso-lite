# virtio-win-iso-lite

**Automated cleaner and rebuilder for the official Fedora virtio-win driver ISOs.**  
Removes developer files and bloat while preserving drivers and guest tools for all supported Windows architectures (amd64, x86, i386, arm64).  
Built and updated automatically using GitHub Actions.

---

## Features

- **Automatic Download**: Always fetches the latest upstream virtio-win ISO from Fedora.
- **Cleans Unneeded Files**: Strips debug symbols, logs, dev/test scripts, and non-essential documentation.
- **All Platform Support**: Keeps all Windows drivers and tools (for QEMU, KVM, Proxmox, etc.), across all architectures.
- **Lightweight Releases**: Smaller ISO with no impact on usability.
- **Open Automation**: Workflow is public and auditable—anyone can fork or customize it.

---

## Download

Get the latest cleaned ISO and archives from the [Releases page](https://github.com/caoquocdung/virtio-win-iso-lite/releases).

---

## What’s Included / What’s Removed

| Item                | Status      |
|---------------------|-------------|
| Drivers (all archs) | ✅ Kept     |
| Guest tools/agent   | ✅ Kept     |
| Debug symbols (.pdb)| ❌ Removed  |
| Dev/test scripts    | ❌ Removed  |
| Log/temp/backup files | ❌ Removed |
| Documentation (non-README) | ❌ Removed |
| README / essential info | ✅ Kept |
| Empty directories   | ❌ Removed  |

---

## Usage

1. **Download** the ISO or archive from the [Releases page](https://github.com/caoquocdung/virtio-win-iso-lite/releases).
2. **Mount or attach** the ISO to your VM, or extract drivers as needed.
3. **Enjoy** a cleaner, lighter package—no loss of end-user functionality.

---

## How It Works

- **This repository runs a GitHub Actions workflow** on a schedule (and on demand).
- The workflow:
    1. **Fetches the latest virtio-win ISO** from Fedora's official repository.
    2. **Extracts and cleans up** files, removing anything not needed by end users.
    3. **Repackages** the ISO and uploads `.iso`, `.tar.gz`, and `.tar.xz` archives to GitHub Releases.

---

## For Developers & Advanced Users

- See `.github/workflows/build.yml` for the full automation logic.
- Fork the repo and customize the workflow if you want to keep/remove additional files.

---

## Why Use This?

- **Save bandwidth and disk space** with smaller ISOs.
- **Cleaner driver media** for use with Windows VMs on QEMU/KVM/Proxmox.
- **No developer/debug files** to confuse or clutter your VM installs.
- **Trust and transparency:** See exactly how each ISO was built, right here on GitHub.

---

## License

This project only redistributes open Fedora virtio-win drivers.  
Workflow and scripts are licensed under the MIT License.  
All driver binaries remain the copyright of their original authors.

---

## Credits

- [Fedora virtio-win project](https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/latest-virtio/) for original driver packages.
- [GitHub Actions](https://github.com/features/actions) for CI/CD automation.

---

**Have an idea or improvement?**  
Feel free to open an Issue or PR!

