# Ditana Config Logseq

This Arch package provides a preconfigured setup of [Logseq](https://logseq.com) with its [GPT-3 OpenAI plugin](https://github.com/briansunter/logseq-plugin-gpt3-openai), tailored for use with a local [KoboldCpp](https://github.com/LostRuins/koboldcpp) instance.

## Description

[Logseq](https://logseq.com) is more than just a note-taking app; it serves as a comprehensive platform for organizing thoughts, managing tasks, and building knowledge databases. In Ditana, Logseq is specially configured to leverage the local AI powered by KoboldCpp. This integration enables AI-assisted note-taking, content generation, and knowledge management, all while maintaining privacy and security.

This package is ideal for anyone looking to enhance their intellectual workflow with the power of AI, without compromising on data privacy.

## Features

- Preconfigured Logseq setup optimized for Ditana GNU/Linux
- Integration with local KoboldCpp instance for AI-powered features
- Privacy-focused configuration, keeping your data local
- Custom shortcuts for quick access to AI features
- Tailored chat prompt for concise and focused AI responses

## Prerequisites

- Ditana GNU/Linux with a desktop environment
- A running KoboldCpp server (can be the [ditana-koboldcpp](https://aur.archlinux.org/packages/ditana-koboldcpp) package)

## Installation

This package is available in the Ditana GNU/Linux Arch repository. It is installed by default with desktop installations.

## Configuration

The package sets up Logseq with the following key configurations:

- GPT-3 OpenAI plugin enabled and configured to use the local KoboldCpp instance
- Custom chat prompt for focused AI responses

You can find the configuration files in the following locations:

- Plugin configuration: `~/.logseq/config/plugins.edn`
- GPT-3 OpenAI plugin settings: `~/.logseq/settings/logseq-plugin-gpt3-openai.json`

## Usage

1. Ensure the KoboldCpp server is running (typically handled automatically by the `ditana-koboldcpp` service)
2. Launch Logseq
3. Use the configured shortcuts to access AI features:
   - `mod+j`: AI block completion
   - `mod+g`: AI popup for queries

## Customization

You can customize the Logseq configuration and GPT-3 OpenAI plugin settings by editing the respective configuration files mentioned in the Configuration section.

## Dependencies

- [logseq-desktop-bin](https://aur.archlinux.org/packages/logseq-desktop-bin)
- A running KoboldCpp instance (provided by `ditana-koboldcpp` in Ditana)

## Support

For issues, feature requests, or contributions related to the Ditana configuration of Logseq, please use the GitHub issue tracker or submit a pull request.

For Logseq-specific questions, refer to the [official Logseq documentation](https://docs.logseq.com/).

## Acknowledgements

This project uses the [logseq-plugin-gpt3-openai plugin](https://github.com/briansunter/logseq-plugin-gpt3-openai) by Brian Sunter. We thank Brian for developing this plugin, which has been valuable in integrating AI capabilities into Logseq for the Ditana project.

---

Ditana Config Logseq is part of the Ditana GNU/Linux project, aiming to provide sophisticated and privacy-focused tools for knowledge management and productivity.
