## Creating Secrets Break Down
- Use docker secret create followed by the name of the secrets file you want to create.
# Ex: CLI
    - docker secret create my_first_secret

## Adding Your Secret Into The File
- You can use the command echo to add your custom secret into the secrets file
- Must know the path to your secret file (typically /run/secrets) 
# Ex: CLI 
    - echo "my_seecret_2024" > /run/secrets/my_first_secret