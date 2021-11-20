# Biohacking

A 'mindmap' aka markdown documentation about biohacking and good practises to energize your body and brain
to function better overall during your day. Don't forget to take your nutritions on daily basis. References of useful
products and practises within Biohacking.

# Requirements

- npm 'node package manager'

# Get started

In order to view the markdown documentation as a mindmap you need to install markmap via yarn package manager.


# Install markmap cli and related dependencies

```bash
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt -y install nodejs
sudo npm install -g yarn
yarn global add markmap-cli
```

# Usage

## Combine the markdown files into one markdown file

```bash
mkdir target
biohacking_index.md doc/*.md > target/biohacking_references.md
```

## Generate html file of the markdown file

```bash
npx markmap-cli target/biohacking_references.md
```

## On the fly generation of the edited markdown file on local running server

```bash
npx markmap-cli -w target/biohacking_references.md
```

## Autogenerate markdown file changes

```bash
mkdir target
while true; do cat biohacking_index.md doc/*.md > target/biohacking_references.md;\
npx markmap-cli target/biohacking_references.md && sleep 60; done
```

## References