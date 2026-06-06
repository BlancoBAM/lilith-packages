# Lilith Linux Package Repository

**APT package repository for Lilith Linux** — hosted on GitHub Pages.

## Add to APT

```bash
# 1. Download and install the GPG signing key
curl -fsSL https://blancobam.github.io/lilith-packages/public-key.asc | \
  sudo gpg --dearmor -o /usr/share/keyrings/lilith-archive-keyring.gpg

# 2. Add the repository source
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/lilith-archive-keyring.gpg] \
  https://blancobam.github.io/lilith-packages stable main xtra" | \
  sudo tee /etc/apt/sources.list.d/lilith-linux.list

# 3. Update and install
sudo apt update
sudo apt install offerings tweakers lilim stake ouija-pad
```

## Components

| Component | Description |
|---|---|
| `main` | Core Lilith Linux packages (installed by default) |
| `xtra` | Optional curated extras |
| `desktop` | Alternative desktop environment meta-packages |

## Packages

Browse the [package landing page](https://blancobam.github.io/lilith-packages/) for the full package list.

## Signing Key

The repository is signed with the Lilith Linux GPG key. Download the public key:
- [public-key.asc](https://blancobam.github.io/lilith-packages/public-key.asc) (GPG public key, ASCII armor)

## Source

Repository spec: [lil-build/lilith-debrep.toml](https://github.com/BlancoBAM/lil-build)
