# Operação do Altímetro

Este documento descreve o funcionamento do altímetro e os procedimentos necessários para sua operação.

---

# Modos de operação

O altímetro possui dois modos de funcionamento:

- **Modo de aquisição de dados**
- **Modo de recuperação de dados**

O modo de operação é definido automaticamente pela forma como o equipamento é energizado.

| Forma de alimentação | Modo selecionado |
|----------------------|------------------|
| Pilha CR2032 | Aquisição de dados |
| Módulo USB-TTL conectado ao computador | Recuperação de dados |

---

# Modo de aquisição de dados

O modo de aquisição é utilizado durante os testes e lançamentos. Nesse modo, o altímetro monitora continuamente a pressão atmosférica, identifica o voo e registra todas as medições na memória EEPROM.

## Inicialização

Ao ligar o equipamento utilizando a pilha CR2032, podem ocorrer duas situações.

### LED verde aceso continuamente

Indica que:

- o altímetro está pronto para um novo voo;
- o sistema está monitorando continuamente a pressão atmosférica;
- a memória está liberada para registrar uma nova aquisição.

Nenhuma ação adicional é necessária.

---

### LED verde piscando

Indica que existe um voo armazenado na memória que ainda não foi liberado pelo programa de recuperação de dados.

Isso significa que ocorreu uma das seguintes situações:

- o altímetro ainda não foi conectado ao computador após o voo;
- os dados foram recuperados, porém não foi utilizada a opção de liberar um novo voo.

Esse comportamento funciona como um mecanismo de proteção, impedindo que um novo lançamento sobrescreva acidentalmente os dados já armazenados.

Enquanto o LED permanecer piscando, um novo voo **não será iniciado**.

Para liberar uma nova aquisição, conecte o altímetro ao computador e utilize a função correspondente no programa de recuperação de dados.

---

## Indicações durante o voo

Embora os LEDs normalmente não sejam visíveis durante um lançamento real, eles são extremamente úteis durante testes em bancada.

### LED verde piscando

Após a identificação do trigger de lançamento, o LED verde passa a piscar, indicando que a aquisição de dados foi iniciada.

---

### LED azul aceso

Quando o sistema identifica o início da trajetória descendente (após o apogeu), o LED azul é aceso.

---

### Final do voo

Quando o altímetro identifica que o foguete não apresenta mais variações de altitude, considera que o voo foi encerrado.

Nesse momento:

- o LED azul é apagado;
- o LED verde volta a piscar na mesma frequência utilizada para indicar voo bloqueado.

Esse estado permanece até que o voo seja recuperado e um novo voo seja liberado pelo software.

---

# Modo de recuperação de dados

O modo de recuperação é utilizado para transferir ao computador os dados registrados durante o voo.

## Inicialização

Para entrar nesse modo, conecte o módulo USB-TTL ao altímetro e, em seguida, conecte-o ao computador.

O altímetro iniciará automaticamente no modo de recuperação.

Quando esse modo é iniciado:

- o LED azul permanece aceso continuamente.

Esse comportamento indica que o equipamento está pronto para comunicação com o computador.

---

## Recuperação dos dados

Todas as operações de recuperação são realizadas por meio do programa de [recuperação de dados](recuperar-dados.md).

Através dele é possível:

- recuperar todas as medições armazenadas na EEPROM;
- salvar os dados no computador;
- liberar a memória para permitir um novo voo.

Após a recuperação dos dados e a liberação de um novo voo pelo software, o altímetro estará novamente apto para operar no modo de aquisição.

← [Voltar ao menu principal](/README.md)