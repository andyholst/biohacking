# biohacking

A 'mindmap' markdown documentation about biohacking

# Requirements

- npm 'node package manager'

# Get started

In order to view the markdown documentation as a mindmap you need to install markmap via yarn package manager.

# Install markmap cli and related dependencies

npm install -g yarn
yarn global add markmap-cli

# Usage

## Combine the markdown files into one markdown file

mkdir target
while true; do cat biohacking_index.md doc/*.md > target/biohacking_references.md && sleep 10; done

## Generate html file of the markdown file once

npx markmap-cli target/biohacking_references.md

## On the fly generation of the edited markdown file on local running server

npx markmap-cli -w target/biohacking_references.md

## Autogenerate markdown file changes

while true; do cat biohacking_index.md doc/*.md > target/biohacking_references.md;\
npx markmap-cli target/biohacking_references.md && sleep 60; done

