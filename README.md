# Setup GitHub project

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

## Milestones 

### Lister les milestones
```bash
gh milestone list
```

## Create an alias for use it in your project

### open your bashrc

```
nano ~/.bashrc
```

### Create your function

```
download_execute_remove() {
    # Link to download
    url="https://raw.githubusercontent.com/MarinCvl/Setup_project_GitHuc_CLI/main/starterIssues"
    
    # Doawnload file from url
    curl -O "$url"
    
    # Extract the name of the downloaded file
    file_name=$(basename "$url")

    # Set execution permissions
    chmod +x "$file_name"
    
    # Execute file
    ./"$file_name"
    
    # Delete the file once execution is complete
    rm "$file_name"
}
```

### Then assign this alias to a shorter command

```
alias dxe='download_execute_remove
```
