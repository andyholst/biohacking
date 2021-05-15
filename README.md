# Biohacking

A 'mindmap' aka markdown documentation about biohacking and good practises to energygize your body and brain
to function better overall during your day. Don't forget to take your neutritions on daily basis.

# Requirements

- npm 'node package manager'

# Get started

In order to view the markdown documentation as a mindmap you need to install markmap via yarn package manager.

# Install markmap cli and related dependencies

```bash
npm install -g yarn
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
while true; do cat biohacking_index.md doc/*.md > target/biohacking_references.md;\
npx markmap-cli target/biohacking_references.md && sleep 60; done
```

## References