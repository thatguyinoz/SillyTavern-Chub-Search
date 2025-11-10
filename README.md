# SillyTavern Chub Search

SillyTavern Chub Search is an which provides a quick and easy way to search for new cards from [CHUB](https://www.chub.ai/about) from the comfort of your tavern. 

![image](https://github.com/city-unit/SillyTavern-Chub-Search/assets/140349364/648e43ae-3ed0-4673-b024-f4ba7846998c)


## Installation and Usage

Utilize SillyTavern's third party extension importer to install.

![image](https://github.com/city-unit/st-auto-tagger/assets/1860540/188b8ba5-c121-4357-96f8-a45bd60cf8a5)

To use the search, click the thunderbolt icon.

![image](https://github.com/city-unit/st-chub-search/assets/140349364/a8857619-54df-43f8-b42d-2635d4c5a412)


## Prerequisites

This extension requires >= SillyTavern commit [01e38be](https://github.com/SillyTavern/SillyTavern/commit/01e38be408b4bd40792c3cf86d353ecad60f7ea2) to function.

## Proxy Requirements (for this Fork)

This forked version of the SillyTavern Chub Search extension requires a companion **server plugin** to route its API requests through a SOCKS5 proxy (e.g., Tor). This is necessary because client-side JavaScript cannot directly configure proxy settings.

### `st-proxy-plugin` Installation

1.  **Install Tor Proxy:** Ensure you have a SOCKS5 proxy (like Tor) running and listening on an accessible IP and port (e.g., `10.99.3.254:19050`). Refer to the `transparent_proxy_chain.md` documentation for Tor installation on Ubuntu.

2.  **Copy Plugin:** Copy the entire `st-proxy-plugin` directory (available in the same repository as this extension) into your SillyTavern installation's `plugins` directory.

    ```bash
    # Example: Assuming SillyTavern is in ~/SillyTavern and st-proxy-plugin is in ~/st-proxy-plugin
    cp -r ~/st-proxy-plugin /path/to/your/SillyTavern/plugins/
    ```

3.  **Install Dependencies:** Navigate into the copied plugin directory on your server and install its Node.js dependencies:

    ```bash
    cd /path/to/your/SillyTavern/plugins/st-proxy-plugin
    npm install
    ```

4.  **Enable Server Plugins:** Ensure that `enableServerPlugins` is set to `true` in your SillyTavern's `config.yaml` file.

5.  **Restart SillyTavern:** Restart your SillyTavern server to load the new plugin.

Once the `st-proxy-plugin` is active, this extension will automatically route its CHUB API calls through the configured SOCKS5 proxy.

## Support and Contributions

If you encounter any issues while using this extension, please file an issue on GitHub. If you'd like to contribute to this project, feel free to fork the repository and submit a pull request.

## License

SillyTavern Chub Search is available under the [MIT License](https://github.com/city-unit/st-chub-search/blob/main/LICENSE).
