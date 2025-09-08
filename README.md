# Obsidian Task Properties Plugin

This is an Obsidian plugin that syncs task statuses into note properties.

![demo](./demo.mp4)

## Motivation

Obsidian v1.9.0 adds Bases feature, which is a powerful way to organize your notes in a structured way. When I was trying to migrate my vault to use Bases for task management, I found that there isn't a way to surface task statuses in note properties. This plugin aims to fill that gap.

## How it works

- It monitors the metadata updates in your vault, and also checks the currently open file.
- For each file that has update, if the file as a `#task` tag, it reads all the tasks in the file, and updates the `progress` property in the frontmatter of the file. `progress` is an object with `total` and `completed` counts.
- You can then configure a formula field in the base to calculate the progress percentage, e.g. `progress.completed / progress.total * 100`.

## Note

This plugin is currently in early development stage. It does not provide any configuration options yet. So if your vault uses `#task` tag and `progress` property for other purposes, this plugin may overwrite them. I recommend you to try this plugin in a test vault before installing into your main vault.

I will be adding configuration options and submit to the Obsidian community plugins list. For now, you can install it manually by cloning this repo into your vault's `.obsidian/plugins` folder, or use the BRAT plugin to install from GitHub.

## License

[BSD Zero Clause License & MIT License](LICENSE)
