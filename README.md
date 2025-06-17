# PLAYNHOST Website

This repository contains the source for the **PLAYNHOST** website built with the [Hugo](https://gohugo.io/) static site generator. It hosts information about game and bot hosting services.

## Prerequisites

- [Hugo](https://gohugo.io/) **extended** edition, version 0.120 or later.

## Building

Pricing information is fetched from the WHMCS API only when Hugo is run in the `production` environment. Regular development builds use the local `data/prices.yaml` file.

Examples:

```bash
hugo --environment production        # regular build
HUGO_ENV=production hugo server      # for development with prices
```

The WHMCS proxy endpoint and currency are configured in `config.toml`:

```toml
whmcsProxyURL   = "https://playnhost.com/billing/api-proxy.php"
defaultCurrency = "USD"
```


## License

This project is licensed under the [MIT License](LICENSE).
