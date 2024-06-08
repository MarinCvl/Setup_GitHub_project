# el-portofolio-de-la-muerte

## Install GitHub CLI

Copy the install :

```
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
&& sudo mkdir -p -m 755 /etc/apt/keyrings \
&& wget -qO- https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```

Then, launch the upgrade :

```
sudo apt update
sudo apt install gh
```

## Install gh extensions

gh milestone : a gh extension for managing GitHub Milestones

```
gh extension install valeriobelli/gh-milestone
```

## Issues

### Lister les issues 
```bash
gh issue list
```

## Labels

### Lister les labels
```bash
gh label list
```
