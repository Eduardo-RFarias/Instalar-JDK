# 1

> O primeiro passo é baixar os binários do jdk em formato tar.gz

- com o terminal na pasta principal do usuário ~/.
  > Para entrar nesse caminho digite cd no terminal.
  - para Linux/x64
    ```bash
    wget https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz
    ```
  - para Linux/AArch64
    ```bash
    wget https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz
    ```

# 2

> Agora é preciso extrair o arquivo baixado

- ainda com o terminal na pasta principal do usuário
- execute o comando:

```bash
tar -xf openjdk-17.0.2_linux-x64_bin.tar.gz
```

> o nome do arquivo pode variar

# 3

- execute o comando

```bash
mkdir .java
mv jdk-17.0.2 .java
```

> Isso vai criar uma pasta chamada .java e mover o arquivo extraido para lá

# 4

- execute o comando

```
nano .bashrc
```

> isso vai abrir no terminal o arquivo .bashrc para que possa edita-lo, use o teclado para navegar e editar o arquivo.

- procure no arquivo se existe alguma linha com `export JAVA_HOME=...` ou `export PATH=.../java/...` e apague se houver.
- Digite no final do arquivo as duas linhas:
  - `export JAVA_HOME="~/.java/jdk-17.0.2"`
  - `export PATH="$JAVA_HOME/bin:$PATH"`

# 5

- Reinicie seu linux e teste os comandos
  ```bash
  java --version
  javac --version
  ```

# 6

- Para instalar os binários do JavaFX é necessário fazer download dos arquivos e move-los para a pasta jmods em sua JAVA_HOME
  - Acesse o [link](https://gluonhq.com/products/javafx/) da gluon e baixe o zip do tipo jmods
  - Extraia o zip dentro da pasta jmods em sua JAVA_HOME, você vai precisar do pacote unzip `sudo apt install unzip`
  - Ex:
    ```bash
    cd $JAVA_HOME/jmods
    wget https://download2.gluonhq.com/openjfx/17.0.2/openjfx-17.0.2_linux-x64_bin-jmods.zip
    unzip -j openjfx-17.0.2_linux-x64_bin-jmods.zip
    rm openjfx-17.0.2_linux-x64_bin-jmods.zip
    ```
  - Ex Linux aarch64:
  ```bash
    cd $JAVA_HOME/jmods
    wget https://download2.gluonhq.com/openjfx/17.0.2/openjfx-17.0.2_linux-aarch64_bin-jmods.zip
    unzip -j openjfx-17.0.2_linux-x64_bin-jmods.zip
    rm openjfx-17.0.2_linux-x64_bin-jmods.zip
  ```
