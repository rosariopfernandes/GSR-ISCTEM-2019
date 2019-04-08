# Exercício (Gestão de Utilizadores)
1. groupadd:
    ```shell
    sudo groupadd -g 1002 lgsr
    ``` 

2. adduser:
    ```shell
    sudo adduser gsr --uid 1003 --ingroup lgsr
    ``` 

3. (Done)

4. userdel:
    ```shell
    sudo userdel gsr
    ``` 

5. adduser:
    ```shell
    sudo adduser rosario --ingroup lgsr
    ``` 


# Exercícios (permissões de ficheiros)
1. touch:
    ```shell
    touch exercicio1.txt
    ```

2. chmod:
    ```shell
    chmod 664 exercicio1.txt
    ```

3. adduser:
    ```shell
    sudo adduser user1 --gid 1001
    ```
    
4. chmod:
    ```shell
    chmod 700 /home/rosariopfernandes
    ```

5. ll:
    ```shell
    ll /usr/bin/passwd
    ``` 

    As permissões são: `-rws r-x r-x`
    
    Qual será a razão para esse ficheiro ter essas permissões?
    
    🤷‍
