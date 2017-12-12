# Encapsulamento

## Ferramenta
> Declarar tudo como privado, então, analisar o código e decidir quais métodos são importantes deixar expostos.

>Nunca expor os campos/atributos da classe, nem setters e nem getters. Quando precisar fazer um getter, retornar um objeto cópia.

>Se mesmo assim, for necessário criar um método setter, deve-se checar antes o valor a ser atribuído e nunca atribuir um valor de referência.

>As outras classes não devem saber como a classe principal faz seu trabalho. As mudanças devem ocorrer em somente um lugar.

>Poder dizer o que o método faz sem dizer como ele faz.


## Inspeção
##### Caso 1 - Encapsulamento
>https://gist.github.com/ProgDan/867654<br>
>Aparentemente está tudo certo.

##### Caso 2 - Encapsulamento 
>https://gist.github.com/martin8115/503707e6c385b54dcb2a7b9e931fb8a1<br>
>Todos os métodos e variáveis são públicos. Ex: fill. É difícil verificar o que está certo/errado, pois como tudo está como público, não temos um controle do que realmente deveria estar exposto.

##### Caso 3 - Encapsulamento
>https://gist.github.com/palmerabollo/7006426<br>
>Todas propriedades estão privadas, todos os métodos internos estão privados e somente os necessários estão públicos.

##### Caso 4 - Encapsulamento
>https://github.com/pettomartino/coursera-ita-java-oo/blob/master/semana-3/src/Pizza.java 
>Métodos e atributos não definidos como public ou private.