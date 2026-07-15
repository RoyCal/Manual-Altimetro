# Instalação do Sistema de Visualização

Esta seção descreve os passos necessários para instalar e configurar o sistema de visualização responsável pela exibição e análise dos dados recuperados do altímetro.

## Pré-requisitos

Antes de prosseguir, certifique-se de que todos os requisitos descritos na página **[Requisitos](requisitos.md)** foram atendidos.

## 1. Obter o sistema de visualização

O código-fonte do sistema de visualização está disponível no seguinte repositório do GitHub:

**https://github.com/RoyCal/Interface-altimetro-TCC**

Caso o Git esteja instalado em seu computador, clone o repositório executando o comando abaixo:

```bash
git clone https://github.com/RoyCal/Interface-altimetro-TCC.git
```

Como alternativa, é possível fazer o download do código-fonte diretamente pelo GitHub utilizando a opção **Code → Download ZIP** e, em seguida, extrair o conteúdo em uma pasta de sua preferência.

## 2. Instalar as dependências

Abra um terminal na pasta raiz do projeto e execute o comando abaixo para instalar todas as dependências definidas no arquivo `package.json`:

```bash
npm install
```

Esse comando realiza o download e a instalação automática de todos os pacotes necessários para o funcionamento da aplicação.

## 3. Configurar o banco de dados

Na pasta raiz do projeto, crie manualmente um arquivo chamado `.env`.

Em seguida, adicione as configurações de acesso ao banco de dados, substituindo os valores conforme a configuração do servidor MySQL:

```text
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=senha_do_mysql
DB_NAME=nome_do_banco_de_dados
```

> **Observação:** o banco de dados não precisa existir previamente no servidor MySQL. A aplicação realiza a criação da estrutura necessária automaticamente durante sua inicialização.

## Conclusão

Após concluir as etapas acima, o sistema de visualização estará devidamente instalado e configurado, estando pronto para ser executado conforme as instruções de utilização.

---

← [Voltar ao menu principal](/README.md)
