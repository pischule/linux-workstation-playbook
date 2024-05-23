## Initial run

1. Update repos && packages

    ```sh
    sudo apt update && sudo apt dist-upgrade
    ```

1. Install ssh server, git

    ```sh
    sudo apt install openssh-server git
    ```

1. Generate ssh keypair

    ```sh
    ssh-keygen -t ed25519 -a 100
    ```

1. Authorize ssh key at Github
   
   Copy to local machine 

    ```sh
    scp your-host:/.ssh/id_ed25519.pub .
    ```

    Add to github.com

1. Run the playbook
    
    ```
    # mkv .venv
    # vrun .venv
    # pip install -r requirements.txt

    ansible-playbook --ask-become-pass main.yml
    ```

1. Relogin

1. Checkout dotfiles

    ```
    dotfiles checkout main
    ```
    