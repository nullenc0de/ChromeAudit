# Overview

This repository contains a collection of Nuclei plugins designed to audit Chrome extensions for potential security vulnerabilities. The plugins are designed to identify and mitigate a variety of issues, including the misuse of wildcards in manifest files, improper sanitization of inputs, the use of potentially dangerous JavaScript methods such as `document.write()` and `innerHTML`, and more. Each plugin provides a detailed explanation of the issue it addresses, along with code examples and regular expressions to identify and extract relevant code snippets.

The plugins also provide guidelines for secure coding practices, such as limiting the use of externally connectable fields, using content scripts carefully, and minimizing the list of web-accessible resources. Additionally, they offer tools to identify and mitigate potential false positives, such as improperly implemented Cross-Origin Resource Sharing (CORS), and to ensure the inclusion of an explicit content security policy in the extension's manifest. The severity of the issues addressed by these plugins ranges from low to medium.

## Technologies and Frameworks

The plugins in this repository are written in YAML and JSON, and are designed to be used with the Nuclei tool. They make extensive use of regular expressions for pattern matching and extraction. The plugins are designed to audit Chrome extensions, and as such, they deal with JavaScript and JSON files. The author of several of these plugins is nullenc0de.

# Installation and use

Follow the steps below to install and start working with the project:

1. **Download the Chrome Extension as a ZIP file**. In case you can only find a CRX file, rename it with the extension [.zip](https://chrome-stats.com).

2. **Unzip the downloaded file** to access its contents.

3. **Execute the Nuclei tool** with the following command:
```
nuclei -target /chrome-ext -t ./templates
```

Replace `/chrome-ext` with the path to the unzipped extension's files.
