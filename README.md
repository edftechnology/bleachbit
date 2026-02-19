# Como configurar/instalar/usar o `BleachBit` no `Linux Ubuntu`

## Resumo

Neste documento estao contidos os principais comandos e configuracoes para configurar/instalar/usar o `BleachBit` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using `BleachBit` on `Linux Ubuntu`._

## 1. Como configurar/instalar/usar o `BleachBit` no `Linux Ubuntu`

Siga os passos abaixo para instalar e utilizar o `BleachBit`:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```



2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```

    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```

    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```


3. Instale o `BleachBit` atraves do gerenciador de pacotes:
   ```bash
   sudo apt install bleachbit -y
   ```
4. Execute o `BleachBit` via _interface_ gráfica ou pelo `Terminal Emulator`:
   ```bash
   bleachbit
   ```
   Para executar como administrador (permitindo uma limpeza mais profunda):
   ```bash
   sudo bleachbit
   ```

### Dicas adicionais

O `BleachBit` possui diversas opcoes de limpeza. Explore as categorias disponiveis e marque apenas o que deseja remover. Sempre revise as opcoes antes de executa-las para evitar a exclusao de dados importantes.

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `bleachbit` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install bleachbit -y
    sudo bleachbit
    ```


## Referências

[1] OPENAI. ***Instalar o `bleachbit` no `linux ubuntu` no `terminal emulator`***. Disponível em: <https://chatgpt.com/c/688abea5-9efc-832f-88f7-baeaeb5f9ec7>. ChatGPT. Acessado em: 31/07/2024.
