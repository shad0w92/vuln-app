
# OWASP Dependency Check CLI Installation on MacBook

## Pré-requisitos

1. **Instalar Java**: Verifique se você tem o Java Runtime Environment (JRE) 8 ou superior instalado. Você pode instalar o Java usando o Homebrew:
   ```bash
   brew install openjdk@11
   ```
   E adicionar o Java ao PATH:
   ```bash
   echo 'export PATH="/usr/local/opt/openjdk@11/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```

## Instalação do OWASP Dependency Check CLI

1. **Download**: Baixe a última versão do OWASP Dependency Check CLI a partir do site oficial. Você pode fazer isso diretamente pelo terminal:
   ```bash
   wget https://github.com/jeremylong/DependencyCheck/releases/download/v7.4.0/dependency-check-7.4.0-release.zip
   ```

2. **Descompactar**: Descompacte o arquivo baixado:
   ```bash
   unzip dependency-check-7.4.0-release.zip
   ```

3. **Mover para um Diretório Adequado**: Mova o diretório descompactado para um local adequado, como `/usr/local/`:
   ```bash
   sudo mv dependency-check /usr/local/
   ```

4. **Adicionar ao PATH**: Adicione o diretório `dependency-check` ao seu PATH. Abra o arquivo de configuração do seu shell (`~/.zshrc` para zsh ou `~/.bash_profile` para bash) e adicione a seguinte linha:
   ```bash
   export PATH="/usr/local/dependency-check/bin:$PATH"
   ```
   Então, recarregue o arquivo de configuração do shell:
   ```bash
   source ~/.zshrc  # para zsh
   source ~/.bash_profile  # para bash
   ```

## Atualizar Banco de Dados

Atualize o banco de dados de vulnerabilidades. Execute o comando:
```bash
dependency-check.sh --updateonly
```

## Executar uma Verificação

Para executar uma verificação em um projeto, use o comando abaixo, substituindo `/caminho/para/o/projeto` pelo caminho do seu projeto:
```bash
dependency-check.sh --project "Meu Projeto" --scan /caminho/para/o/projeto
```

## Resumo dos Comandos

Aqui está um resumo dos comandos que você precisará executar no terminal do seu MacBook:

1. Instalar Java:
   ```bash
   brew install openjdk@11
   echo 'export PATH="/usr/local/opt/openjdk@11/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```

2. Baixar e descompactar o OWASP Dependency Check CLI:
   ```bash
   wget https://github.com/jeremylong/DependencyCheck/releases/download/v7.4.0/dependency-check-7.4.0-release.zip
   unzip dependency-check-7.4.0-release.zip
   sudo mv dependency-check /usr/local/
   ```

3. Adicionar ao PATH:
   ```bash
   echo 'export PATH="/usr/local/dependency-check/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```

4. Atualizar o banco de dados:
   ```bash
   dependency-check.sh --updateonly
   ```

5. Executar uma verificação:
   ```bash
   dependency-check.sh --project "Meu Projeto" --scan /caminho/para/o/projeto
   ```

Seguindo esses passos, você deverá conseguir instalar e usar o OWASP Dependency Check CLI no seu MacBook.
