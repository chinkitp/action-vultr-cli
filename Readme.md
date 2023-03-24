# Github Action for Vultr

The action enables you to interact with Vultr services throught the vultr-cli.

## Example usage

```yaml
jobs: 
  Deploy-Infrastructure:
    runs-on: ubuntu-latest
    steps:
    - name: Login to vultr
      uses: chinkitp/action-vultr-cli@v1.3
      with:
      # Vultr API Key
        token: ${{ secrets.VULTR_API_KEY }}

    - name: Create Infrastructure        
      run: vultr-cli vpc list
```

## Build 

```bash
ncc build index.js --license licenses.txt
```

## Credits
- Forked from https://github.com/techknowlogick/action-vultr
- https://github.com/digitalocean/action-doctl 