# Doppler Environment Loader

A GitHub Action to load Doppler secrets into the environment

# Usage

## Dependencies on other GitHub Actions

- The Doppler CLI must be loaded before this action using [dopplerhq/cli-action](https://github.com/marketplace/actions/install-doppler-cli)

## Inputs

Action configuration settings to be used within the `with` block.

- doppler-token - The Doppler project access token

  - Required
  - Example
    ```
    with:
      doppler-token: ${{ secrets.DOPPLER_TOKEN_DEV }}
    ```

- debug-prefix - The prefix of the environment variable's that won't be masked

  - Default: `DEBUG`
  - Example
    ```
    with:
      doppler-token: ${{ secrets.DOPPLER_TOKEN_DEV }}
      debug-prefix: 'DBG'
    ```

- disable-masking - Whether to disable all masking of secrets in the action
  - Default: `false`
  - Example
    ```
    with:
      doppler-token: ${{ secrets.DOPPLER_TOKEN_DEV }}
      disable-masking: 'false'
    ```

## Sample

```
- name: Load environment variables
  uses: catchco/doppler-environment-loader@latest
  with:
    doppler-token: ${{ secrets.DOPPLER_TOKEN_DEV }}
    debug-prefix: 'DBG'
    disable-masking: 'false'
```
