# Introdução 
---
Framework JAVA criado para facilitar o desenvolvimento de testes automatizados, bem como aumentar a produtividade e a padronização do desenvolvimento de rotinas de testes automatizados.

## Comandos Básicos Web
---
Classe responsável por por conter comandos que executam interações em páginas web. Os métodos contidos na classe sãoo todos públicos e para utiliza-los, não é necessário passar o WebDriver como parametro.

Possui as seguintes propriedades: 

<code>**WebDriver**</code> driver

<code>**Actions**</code> action

<code>**WebDriverWait**</code> wait

E comporta os seguintes métodos:

### ComandosBasicos
---
Método construtor da classe que recebe o **WebDriver** como parâmetro.

Ex:

```JAVA
ComandosBasicos comBasico = new ComandosBasicos(driver);
```

### mudarAba
---
Método resposanvel por mudar a aba atual do navegador recebe um <code>**int**</code> como parâmetro, as abas são lidas em um array dessa forma, são zero indexadas, ou seja, os números passados vão de 0 à quantidade de abas abertas no momento menos 1.

> <span style="color: blue;">**Parâmetro**</span>: <code>int</code> indiceAba

Ex:

```JAVA
ComandosBasicos comBasico = new ComandosBasicos(driver);
comBasico.mudarAba(0);
```

No exemplo acima mudamos navegamos para a primeira aba do navegador.

Caso seja informado o indice uma aba inexistente como parâmetro será lançada a seguinte <code>**Exception**</code>:

> <span style="color: red;">**Exception**</span>: Este Indice de Aba não existe! Use um valor Valido!


### trocarJanela
---
Método responsável trocar a janela ativa do navegador que recebe um <code>**int**</code> como parâmetro, as janelas são lidas em um array dessa forma, são zero indexadas, ou seja, os números passados vão de 0 à quantidade de abas abertas no momento menos 1.

> <span style="color: blue;">**Parâmetro**</span>: <code>int</code> indiceJanela

Ex:

```JAVA
ComandosBasicos comBasico = new ComandosBasicos(driver);
comBasico.trocarJanela(0);
```

No exemplo acima mudamos navegamos para a primeira janela ativa.

Caso seja informado o indice uma janela inexistente como parâmetro será lançada a seguinte <code>**Exception**</code>:

> <span style="color: red;">**Exception**</span>: Este Indice de janela não existe! Use um valor Valido!


### borda
---
Método responsável por localizar um elemento no navegador e destacar o mesmo com um borda vermelha para exibir qual fluxo ou ação está sendo realizado, recebe um <code>**WebElement**</code> como parâmetro.

Ex:

```JAVA
ComandosBasicos comBasico = new ComandosBasicos(driver);
WebElement menuLink = comBasico.encontra("menu-link");
comBasico.borda(menuLink);
```
