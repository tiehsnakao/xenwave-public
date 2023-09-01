# Xenwave Public Data Repository

Welcome to the Xenwave Public Data Repository! This is the official repository for hosting public data utilized by the Xenwave Protocol. The aim is to create a seamless, transparent, and easy-to-navigate platform for all contributors. If you wish to get involved, here are some ways you can contribute:

- Add your token to the `default.json` tokens list.
- Register your token details and logo.
- Create and manage custom token lists compatible with Xenwave.

## Table of Contents

1. [Token Lists](#token-lists)
2. [Default List](#default-list)
3. [Token JSON Schema](#token-json-schema)
4. [Custom Lists](#custom-lists)
    - [Custom Token Lists Schema](#custom-token-lists-schema)
5. [Token Information](#token-information)

## Token Lists

Token lists are JSON files with the `.json` extension. These files contain essential information for tokens following the BTS20, BTS21, or ERC20 standards. This enables them to be easily displayed and traded on Xenwave without manual addition.

Xenwave primarily uses a default list but also allows users to create and manage custom token lists.

## Default List

For the default tokens list, Xenwave relies on **[_data/_tokenLists/default.json](/_data/_tokenLists/default.json)**.

If you want your token to be included in this list, please make sure it fulfills the following requirements:

- Sufficient available liquidity and trading volume.
- A credible and functional project, backed by at least a website.
- A trading history of at least 30 days.

The final decision for inclusion is subjective and based on other qualitative assessments. Your project needs to convincingly demonstrate its validity and potential for growth.

> ⚠ **Note**: Remember to also submit your token details and a logo with a transparent background to `/_data/_tokenInfo`. The token information should be placed inside the respective network ID folder (210: Bitnet, or 550: Blockwave Testnet).

## Token JSON Schema

Here's the JSON schema you need to follow for the default token list:

```json
{
    "tokens": [
        {
            "chainId": 210,
            "address": "0xAddress",
            "symbol": "SYMBOL",
            "name": "Token Name",
            "decimals": 18,
            "logoURI": "Logo URL",
            "tags": ["tags"]
        }
    ]
}
```

## Custom Lists

If you prefer to create your own custom token list, you can submit a pull request containing a properly formatted `.json` file to the **[_data/_tokenLists](/_data/_tokenLists/)** directory. We will review and add lists that comply with the correct schema.

### Custom Token Lists Schema

The schema for a custom token list is as follows:

```json
{
    "name": "List Name",
    "logoURI": "Logo URL",
    "keywords": ["tags"],
    "timestamp": "2023-10-01T18:18:00+00:00",
    "version": {
        "major": 1,
        "minor": 0,
        "patch": 0
    },
    "tokens": [
        {
            "chainId": 210,
            "address": "0xAddress",
            "symbol": "SYMBOL",
            "name": "Token Name",
            "decimals": 18,
            "logoURI": "Logo URL",
            "tags": ["tags"]
        }
    ]
}
```

## Token Information

You can also submit your token information for display across our platforms. To do this, please submit a pull request with your token details to `/_data/_tokenInfo/{NETWORK ID}`. Create a directory with your token address, and inside that directory, add a logo in `.png` format with a transparent background, along with a `token.json` file following this schema:

```json
{
    "chainId": [550],
    "address": "0x8148b71232162ea7a0b1c8bfe2b8f023934bfb58",
    "symbol": "WBTN",
    "name": "Wrapped Bitnet",
    "decimals": 18,
    "tags": ["wrapped", "bitnet"]
}
```

## Contributing

If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcomed.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
