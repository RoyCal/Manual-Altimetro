# Como utilizar o Sistema de Visualização de dados

Esta seção descreve como utilizar o sistema de visualização responsável pela exibição e análise dos dados do altímetro.

Antes da utilização do Sistema de Visualização, certifique-se de ter instalado corretamente o sistema através do [guia de instalação](/visualizacao.md).

## Execução utilizando o arquivo executável (Windows)

Para usuários do Windows, a forma recomendada de iniciar o sistema de visualização é utilizando o arquivo executável `sistema.exe`.

Esse arquivo realiza automaticamente a abertura do terminal, a inicialização do servidor de desenvolvimento do Next.js por meio do comando `npm run dev` e, após alguns segundos, abre o navegador padrão no endereço:

```text
http://localhost:3000
```

O arquivo `sistema.exe` deve obrigatoriamente permanecer no mesmo diretório do projeto. **Não altere o local do executável**, pois isso pode impedir seu funcionamento correto.

Caso seja desejado, é possível criar um atalho para o arquivo `sistema.exe` e posicioná-lo em outro local do computador, como a área de trabalho ou o menu iniciar. Entretanto, o arquivo executável original deve permanecer junto aos arquivos do sistema.

## Execução manual pelo terminal

Caso o arquivo executável não esteja disponível ou o usuário prefira iniciar o sistema manualmente, a aplicação pode ser iniciada manualmente pelo terminal.

Primeiramente, abra um terminal na pasta raiz do sistema de visualização, onde está localizado o arquivo `package.json`.

Em seguida, execute o comando:

```bash
npm run dev
```

Após a inicialização do servidor, abra o navegador de internet e acesse:

```text
http://localhost:3000
```

O sistema de visualização será carregado no navegador.

---

← [Voltar ao menu principal](/README.md)
