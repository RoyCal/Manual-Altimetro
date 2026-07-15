# Como utilizar o Programa de Recuperação de Dados

Esta seção descreve como utilizar o aplicativo de terminal responsável pela comunicação com o altímetro.

Antes da utilização do Programa de Recuperação de Dados, certifique-se de ter instalado corretamente através do [guia de instalação](/terminal.md).

## Execução utilizando o arquivo executável (Windows)

Para usuários do Windows, a forma recomendada de iniciar a aplicação é utilizando o arquivo executável `terminal.exe`.

Esse arquivo realiza automaticamente a abertura do terminal e a execução do aplicativo, sem a necessidade de executar comandos manualmente.

O arquivo `terminal.exe` deve obrigatoriamente permanecer no mesmo diretório da aplicação. **Não altere o local do executável**, pois isso pode impedir seu funcionamento correto.

Caso seja desejado, évocê pode criar um atalho para o arquivo `terminal.exe` e posicioná-lo em outro local do computador, como a área de trabalho ou o menu iniciar. Entretanto, o arquivo executável original deve permanecer junto aos arquivos da aplicação!

## Execução manual pelo terminal

Caso o arquivo executável não esteja disponível ou o usuário prefira iniciar o sistema manualmente, a aplicação pode ser iniciada manualmente pelo terminal.

Primeiramente, abra um terminal na pasta raiz da aplicação. Em seguida, execute o arquivo `terminal_ui.py` utilizando o interpretador Python:

```bash
py .\terminal_ui.py
```

Em alguns sistemas, o comando `py` pode não estar disponível. Nesse caso, utilize uma das alternativas:

```bash
python .\terminal_ui.py
```

ou

```bash
python3 .\terminal_ui.py
```

O comando correto depende da configuração do Python no sistema operacional utilizado.

Após a execução do comando, a interface do aplicativo de terminal será iniciada.

---

← [Voltar ao menu principal](/README.md)
