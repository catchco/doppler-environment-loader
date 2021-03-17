# Doppler Environment Loader
A GitHub Action to load Doppler secrets into the environment


# Usage
## Dependencies on other GitHub Actions
* The Doppler CLI must be loaded before this action using [dopplerhq/cli-action](https://github.com/marketplace/actions/install-doppler-cli)

## Sample
```
- name: Load environment variables
  uses: catchco/doppler-environment-loader@latest
  with:
    doppler-token: ${{ secrets.DOPPLER_TOKEN_DEV }}
```
