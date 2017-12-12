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

# Herança

## Ferramenta
> Somente colocar na classe o que diz respeito a ela

> Não possuir repetição de código

> A classe filha deve usar todas as propriedades da classe pai

> Atributos protegidos para que a classe filha possa manipular atributos da classe pai.


## Inspeção
##### Caso 1 - Herança
>https://github.com/pagseguro/java/tree/c4522e24c98ddbd9dadc704424695609fb6aba1d/source/pagseguro-api/src/br/com/uol/pagseguro/domain/direct<br>
Nas classes BoletoPaymentRequest.java, CreditCardPaymentRequest.java, foi feito herança da forma correta, onde elas estendem a classe PaymentRequest, pois as mesmas possuem a mesma base de funcionamento, somente a forma de pagamento é diferente.

##### Caso 2 - Herança
>https://github.com/JanineFreitas/Jogo/tree/master/Jogo/src/jogo<br>
Neste caso existem as classes Peixe.java e Urso.java que estendem a classe Critatura.java. O único método usado as duas classes é o colidir(Ecossistema ecossistema, int posicaoAtual). Porém, ele foi criado como público retornado sempre false. Como ele deveria ser implementado nas classes que o implementam, deveria ter sido criado como abstrato.

##### Caso 3 - Herança
>https://github.com/andres84/superMercadoJPA/tree/master/superMercadoJPA/src/main/java/com/mercado/modelo<br>
Neste caso não foi implementado herança onde poderia ter sido usado. Por exemplo, existem as classes Empleado.java e Cliente.java, que possuem propriedades como nome, sobrenome, endereço, telefone, entre outras que são comum entre as duas classes. Poderia ser sido feita uma classe de Pessoa com as propriedades iguais entre as duas classes, e depois nas classes filhas somente as propriedades diferentes entre as duas.

##### Caso 4 - Herança
>https://github.com/Gutenbergf/Portal-De-Compras/tree/master/src/pkgClasses<br>
Neste caso não houve utilização de herança. A classe Fornecedor.java possui as propriedades de login e senha, que se resumem a classe de Usuario.java, que é formada por somente essas duas propriedades. Portanto, a classe de Fornecedor.java poderia facilmente ser uma extensão da classe de Usuario.java.


# Polimorfismo

## Ferramenta
> A classe de base possui o forma como o processo funciona.

> A classe filha implementa as regras do funcionamento definido nos processos da classe base.

> Os métodos da classe pai devem/podem ser construídos na classe filha

## Inspeção
##### Caso 1 - Polimorfismo
>https://github.com/fernandogalloro/java-jogo-alientrix/tree/master/src/fernando/alientrix<br>
Neste caso, as classes Nave.java, Inimigo.java e Missel.java estendem a classe Movel.java, onde os métodos foram criados corretamente como abstratos e as propriedades protegidas.

##### Caso 2 - Polimorfismo
>https://github.com/Josebr1/Jogo-das-Palavras-Embaralhadas-ITA/tree/master/src/br/com/jose/embaralhador<br>
Neste caso, as classes PalavraInversa.java e PalavraTrocaParImpart.java implementam a interface Embaralhador.lava, que por sua vez possui o método de embaralhar que deve ser implementado pelas classes que o implementam, o que está correto.

##### Caso 3 - Polimorfismo
>https://github.com/ivanknow/venda-agua/tree/master/src/LojaAgua/controlador<br>
Neste caso, o AbstractController.php foi utilizado para fazer o DAO padrão, e as classes de PedidoController.php e UsuarioController.php implementaram o processo de inclusão do registro. O DAO padrão faz o tratamento dos dados, e as classes que o implementam dizem como é feito o processo de inclusão.

##### Caso 4 - Polimorfismo
>https://github.com/pedrug19/VendaVeiculo/tree/master/src/vendaveiculo<br>
Neste caso, a classe abstrata Vendedor.java foi criada corretamente com as propriedades protegidas e com os dados padrões, e suas filhas VendedorGerente, VendedorJunior e VendedorSenior implementam suas particularidades, e são obrigadas a implementar o método verTudo() para exibir os dados conforme o tipo do vendedor.
Somente os getters e setters de todas as propriedades não deveriam ter sido feitos, pois não são utilizados.