# ChromeAudit
[Nuclei](https://github.com/projectdiscovery/nuclei#readme) plugins to audit Chrome extensions

1. **Download the Chrome Extension as a ZIP file**. In case you can only find a CRX file, rename it with the extension .zip.

2. **Unzip the downloaded file** to access its contents.

3. **Execute the Nuclei tool** with the following command:
```
nuclei -target /chrome-ext -t ./templates
```

Replace `/chrome-ext` with the path to the unzipped extension's files and `./temp
