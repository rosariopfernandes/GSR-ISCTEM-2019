# Exercícios Aula 8 Permissões

1. Como utilizador normal, crie um directório "~/permissions". Crie
 um ficheiro nesse directório.
    ```bash
    mkdir ~/permissions
    touch ~/permissions/ficheiro.txt    
    ```

2. Copie um ficheiro do utilizador root do /etc/ para o seu directório "permissions",
 quem é o proprietário do ficheiro agora?
    ```bash
    cp /etc/rsyslog.conf ~/permissions/ 
    ```
    O proprietário do ficheiro copiado sou eu. 😁
    
3. Como root, crie um ficheiro no directório "~/permissions"
    ```bash
    sudo touch /home/<username>/permissions/ficheiroroot.txt
    ```

4. Como utilizador normal, verifique quem é o proprietário do ficheiro criado pelo root.
    ```bash
    ll ~/permissions
    ```
    O proprietário é o root.

5. Torne-se o proprietário de todos os ficheiros no directório "~/permissions".
    ```bash
    chown <username> ~/permissions/*
    ```
    Não é possível tornar-se proprietário dos ficheiros do utilizador root.

6. Certifique-se que tem todas as permissões para estes ficheiros, enquanto outros só podem ler.
    ```bash
    chmod 755 *
    chmod 644 *.txt
    ```
    (Não foi testado)

7. Utilizando `chmod`, `770` é o mesmo que `rwxrwx---` ?
    Sim

8. Utilizando `chmod`, `664` é o mesmo que `r-xr-xr--` ?
    Não

9. Utilizando `chmod`, `400` é o mesmo que `r--------` ?
    Sim

10. Utilizando `chmod`, `734` é o mesmo que `rwxr-xr--` ?
    Não

12. Crie um ficheiro como root, dando só permissão de leitura ao grupo others.
 Utilizadores normais podem ler este ficheiro? Experimente escrever neste ficheiro
 utilizando `vi`.
    ```bash
    sudo su
    touch root.txt
    echo hello > /home/<username>/root.txt
    chmod 744 /home/<username>/root.txt
    exit
    vi ~/root.txt
    ```
    TODO

13. a) Crie um ficheiro como utilizador normal, dando só permissão de leitura ao grupo others.
 Utilizadores normais podem ler este ficheiro? Experimente escrever neste ficheiro utilizando `vi`.
    ```bash
    touch ficheiro13.txt
    echo hello > ficheiro13.txt
    chmod 744 ficheiro13.txt
    ```
    Sim, outros podem ler este ficheiro.

13. b) O utilizador root pode ler este ficheiro? Pode escrever neste ficheiro utilizando o `vi`?
    Sim, root pode ler e escrever neste ficheiro. O sistema de permissões não aplicam-se para este utilizador.
    
14. Criar um directório que pertence a um grupo, onde todos os membros do grupo podem ler e escrever ficheiros,
 e criar ficheiros. Certifique-se que as pessoas possam eliminar apenas os seus próprios ficheiros.
    ```bash
    mkdir /home/project14
    groupadd project14
    chgrp project14 /home/project14
    chmod 775 /home/project42
    ```
