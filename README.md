# Doppler Environment Loader
A GitHub Action to load Doppler secrets into the environment

# Usage
```
- name: Load environment variables
  uses: catchco/doppler-environment-loader@latest
  with:
    doppler-token: ${{ secrets.DOPPLER_TOKEN_DEV }}
```
