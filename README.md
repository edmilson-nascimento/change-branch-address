# Atualização de Endereço (filial) #

[![N|Solid](https://wiki.scn.sap.com/wiki/download/attachments/1710/ABAP%20Development.png?version=1&modificationDate=1446673897000&api=v2)](https://www.sap.com/brazil/developer.html)

Afim de corrigir ~~um problema~~ uma melhoria referente a exibição do SmartForms, sera atualizado o endereco do `local de negocios`. Este pode ser feito seguindo os passos abaixo:

* [Definir local de negocio](#definir-local-de-negocio)

## Definir local de negocio ##


[![N|Solid](https://uploaddeimagens.com.br/images/002/355/670/original/step-01.png](https://www.sap.com/brazil/developer.html)
Para que fique melhor o entendimento, optei por colocar menos informações e mais funcionalidades. A tabela `MAKT - Textos breves de material` foi escolhida apenas por ser relacionada ao modulo que eu tratava quando desenvolvi a solução.






### public section ###
Métodos da sessão publica.
#### search ####
Este tem como objetivo buscar no banco de dados as informações para que sejam exibidas no relatório.
```abap
method search .
```
