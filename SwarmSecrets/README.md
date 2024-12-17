# Creating Secrets Break Down
- Use docker secret create followed by the name of the secrets file you want to create.
## Ex: CLI
    - docker secret create my_first_secret 

# Adding Your Secret Into The File
- You can use the command echo to add your custom secret into the secrets file
- Must know the path to your secret file (typically /run/secrets/<your_secreet_name>) 
## Ex: CLI 
    - echo "my_secret_2024" > /run/secrets/my_first_secret

# Combining Echo + Docker Secret
- You can simplify these steps into one step with a pipeline.
- You will also need to add a dash at the end of the command
    - A dash at the end tells the command to get its input directly from what you type instead of reading from a file.
## Ex: CLI
    - echo "my_secret_2024" | docker secret create my_first_secret -