# Instalar-JDK

Tutorial de instalação da distribuição java OpenJDK + JavaFX e breve guia para compilar o [jabref](https://github.com/JabRef/jabref.git).

# Windows 10

[Clique aqui](./windows.md)

# Linux

[Clique aqui](./linux.md)

# Compilando o jabref

- Clone o projeto do github
- Abra um terminal dentro da pasta do projeto
- digite no terminal:

  ```
  ./gradlew assemble
  ```

- se quiser compilar e testar é só digitar:

  ```
  ./gradlew build
  ```

  (provavelmente vai falhar alguns testes)

- para executar o programa é:

  ```
  ./gradlew run
  ```

  (não funciona no wsl pois o programa tem uma interface gráfica)

- para saber quais são todos os comandos:

  ```
  ./gradlew tasks
  ```

# Bibliografia

[Jabref dev docs](https://devdocs.jabref.org/getting-into-the-code/guidelines-for-setting-up-a-local-workspace)
