# Encapsulamento

## Definições
> Técnica utilizada para esconder uma ideia, ou seja, não expor detalhes internos para o usuário, tornando partes do sistema mais independentes possível. 
DevMedia <http://www.devmedia.com.br/abstracao-encapsulamento-e-heranca-pilares-da-poo-em-java/26366>

> Encapsulamento vem de encapsular, que em programação orientada a objetos significa juntar o programa em partes, o mais isoladas possível. A ideia é tornar o software mais flexível, fácil de modificar e de criar novas implementações.
Wikipédia: Michael Lee Scott, Programming language pragmatics, Edition 2, Morgan Kaufmann, 2006, ISBN 0126339511, p. 481: "Encapsulation mechanisms enable the programmer to group data and the subroutines that operate on them together in one place, and to hide irrelevant details from the users of an abstraction."; Nell B. Dale, Chip Weems, Programming and problem solving with Java, Edition 2, Jones & Bartlett Publishers, 2007, ISBN 0763734020, p. 396.

> É uma forma eficiente de proteger os dados manipulados dentro da classe, além de determinar onde esta classe poderá ser manipulada.
DevMedia <http://www.devmedia.com.br/encapsulamento-polimorfismo-heranca-em-java/12991>

> É uma forma de garantir que as propriedades não serão acessadas/manipuladas sem ter permissão. O que pode ser manipulado estará disponível pelos métodos públicos. O que será manipulado somente para a classe estará como privado e não precisa de um getter/setter necessariamente.
UDESC, Engenharia de Software, 2016.


## Exemplos
##### Caso 1 - Encapsulamento
>https://gist.github.com/ProgDan/867654

##### Caso 2 - Encapsulamento 
>https://gist.github.com/martin8115/503707e6c385b54dcb2a7b9e931fb8a1

##### Caso 3 - Encapsulamento
>https://gist.github.com/palmerabollo/7006426

##### Caso 4 - Encapsulamento
>https://github.com/pettomartino/coursera-ita-java-oo/blob/master/semana-3/src/Pizza.java


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