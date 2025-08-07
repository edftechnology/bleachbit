# Como configurar/instalar/usar o `BleachBit` no `Linux Ubuntu`

## Resumo

Neste documento estao contidos os principais comandos e configuracoes para configurar/instalar/usar o `BleachBit` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using `BleachBit` on `Linux Ubuntu`._

### Descrição [2]

#### `bleachbit`

O `BleachBit` é uma ferramenta gratuita e de código aberto para limpeza e manutenção do sistema operacional Linux (e também Windows), projetada para liberar espaço em disco, remover arquivos temporários, cookies, histórico de navegação, cache de aplicativos e outros dados desnecessários que se acumulam com o uso do sistema. Ele oferece uma interface gráfica intuitiva, além de uma versão em linha de comando, permitindo tanto usuários iniciantes quanto avançados realizarem limpezas seguras e detalhadas. O `BleachBit` suporta dezenas de aplicativos populares (como Firefox, Chromium, LibreOffice, entre outros) e pode ser usado como alternativa ao CCleaner em sistemas Linux, com foco em privacidade e desempenho.

## 1. Instalar o `pdftotext` no `Linux Ubuntu`

Para instalar o `pdftotext`, siga os passos abaixo:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

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

2. Instale o `BleachBit` atraves do gerenciador de pacotes:
   ```bash
   sudo apt install bleachbit -y
   ```
3. Execute o `BleachBit` via interface grafica ou pelo terminal:
   ```bash
   bleachbit
   ```
   Para executar como administrador (permitindo uma limpeza mais profunda):
   ```bash
   sudo bleachbit
   ```

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `bleachbit` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install bleachbit -y
    ```


### Dicas adicionais

O `BleachBit` possui diversas opcoes de limpeza. Explore as categorias disponiveis e marque apenas o que deseja remover. Sempre revise as opcoes antes de executa-las para evitar a exclusao de dados importantes.

## Referencias

[1] OPENAI. ***Instalar BleachBit no Ubuntu***. Acessado em: 31/07/2024.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 25/07/2024 13:33.
