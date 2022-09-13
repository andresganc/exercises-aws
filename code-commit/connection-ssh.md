
## Crear llaves SSH

    1. El comando genera una llave publica y otra privada en la carpeta personal .ssh

        $ ssh-keygen -t rsa -b 4096 -C "andresganc@gmail.com"


    2. Debe verificar que tendo ssh corriendo

        $ eval $(ssh-agent -s)
            answer: Agent pid 4724

    3. Agrego la llave privada al sistema ssh local (Propio)

        $ ssh-add /home/andres/.ssh/id_rsa
            answer: identity added


    4a. Para configurar en AWS

        - https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-ssh-unixes.html?icmpid=docs_acc_console_connect_np

        - Pasos

            1. In the IAM console, in the navigation pane, choose Users, and from the list of users, choose your IAM user.

            2. On the user details page, choose the Security Credentials tab, and then choose Upload SSH public key.

            3. Paste the contents of your SSH public key into the field, and then choose Upload SSH public key.

            4. Copy or save the information in SSH Key ID (for example, APKAEIBAERJR2EXAMPLE).


    4b. Para confirar en github

        - 

