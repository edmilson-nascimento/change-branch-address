# Atualização de Endereço (filial) #

[![N|Solid](https://wiki.scn.sap.com/wiki/download/attachments/1710/ABAP%20Development.png?version=1&modificationDate=1446673897000&api=v2)](https://www.sap.com/brazil/developer.html)

Afim de corrigir um problema com exibiçao do 

Existem vários exemplos e modelos diferente de usar a classe `CL_GUI_ALV_GRID` para exibir relatórios ALV. Sempre que a classe é utilizada, ela necessita de um `container` para que o ALV seja exibido. Ao invés de criar um `container` pra isso, eu preferi utilizar o próprio `container`, que é gerado quando se cria a tela `1000` em um relatório, que no caso, é a tela de seleção. Sim, eu ~~posso~~ vou utilizar o container na tela de seleção para exibir o ALV como eu aprendi com [Gerson Lívio](mailto:gerson@litsolutions.com.br).
A funcionalidade de `SELECT ROWS` foi implementada tambem e será utilizada para selecionar as linhas referentes as ações que desejo fazer.

Para isso eu criei uma classe local básica `GCL_REPORT` com os seguintes métodos:


* [Definir local de negocio](#search)

## Definir local de negocio ##


[![N|Solid](https://uploaddeimagens.com.br/images/002/355/670/original/step-01.png](https://www.sap.com/brazil/developer.html)
Para que fique melhor o entendimento, optei por colocar menos informações e mais funcionalidades. A tabela `MAKT - Textos breves de material` foi escolhida apenas por ser relacionada ao modulo que eu tratava quando desenvolvi a solução.

### public section ###
Métodos da sessão publica.
#### search ####
Este tem como objetivo buscar no banco de dados as informações para que sejam exibidas no relatório.
```abap
method search .
