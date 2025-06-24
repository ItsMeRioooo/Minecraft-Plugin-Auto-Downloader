# Minecraft Plugin Auto Downloader

This project is an auto downloader for Minecraft plugins. It retrieves plugin files from specified links in a configuration file and saves them in a folder named with the current date.

## Project Structure

```
minecraft-plugin-downloader
├── src
│   ├── downloader.py
│   └── __init__.py
├── config
│   ├── plugins.txt
│   └── cookies.txt
├── requirements.txt
└── README.md
```

## Installation

1. Clone the repository or download the project files.
2. Navigate to the project directory.
3. Install the required dependencies using pip:

   ```
   pip install -r requirements.txt
   ```

## Configuration

- Edit the `config/plugins.txt` file to add the names and download links of the Minecraft plugins you want to download.  
  **Format:**  
  ```
  PluginName=https://example.com/plugin-download-link
  ```
  Lines starting with `#` are treated as comments and ignored.

- *(Optional)* If you need to download from sites that require authentication (like BuiltByBit or SpigotMC), add your cookies to `config/cookies.txt` in Netscape format.

## Usage

To run the auto downloader, execute the following command in your terminal:

```
python src/downloader.py
```

This will create a new folder named with the current date and download all specified plugins into that folder.

## Dependencies

- `Python`: Base Language for the Script
- `cloudscraper`: For handling Cloudflare-protected downloads.
- `datetime`: For managing date-related functionalities.

## License

This project is open source and available under the MIT
