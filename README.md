# Desenvolvendo sua aplicação com C# usando DDD

> Alexandre Bogiani Daccas de Mendonça

## Conceito sobre DDD

DDD não é uma metologia, ou um framework estruturado. É uma abordagem de desenvolvimento de software de atacar o processo de concepção do software a partir de um modelo de domínio.

Domínio é conhecimento sobre um certo negócio, ou no escopo do desenvolvimento de software, o conhecimento sobre as diferentes regras de negócio envolvidas no processo a ser atacado no projeto.

Embora não exista um processo estruturado para essa abordagem, existem algumas técnicas e padrões que podem auxiliar no processo de desenho de um projeto de software.

O pilar central do DDD é o conceito de abstração da OOP: como traduzir as regras de negócio para o mundo do desenvolvimento de software.

**Principios do DDD**:

* Alinhamento do código com o negócio
* Favorecer reutilização
* Mínimo de acoplamento
* Independência da Tecnologia

## Criando um modelo de domínio (MDD)

A meta de seu modelo de domínio é reproduzir fielmente seu domínio e as regras de negócio pertencentes a ele, e somente as as que realmente pertencem a ele.

Note que aqui não entra nenhum conceito de tecnologia, integrações, etc. O objetivo é desenhar as regras de negócio, suas propriedades e conexões entre elas. O desenho das classes pode fazer parte desse processo, mas note que a participação do negócio é primordial nessa etapa. Portanto, é extremamente necessário ater-se a uma linguagem clara e úbiqua para todos os envolvidos.

O modelo é vivo, e é trabalhado durante todo o ciclo de vida de desenvolvimento, assim como durante os aperfeiçoamentos da aplicação.

Ao iniciar o desenho da sua aplicação, é preciso isolar o domínio de negócio das demais camadas do sistema. Para isso, você pode usar o conceito de camandas para dividir a aplicação em:

* Interface do Usuário
* Aplicação - não possui regra de negócio, só provê as conexões entre a camada de apresentação e camadas inferiores.
* Dominio - aqui, e somente aqui, entram as regras de negócio e lógica da aplicação. O DDD se concentra nessa camada.
* Infraestrutura

## Regras para modelagem

* Entidades: classes de objetos de seu domínio, que representam elementos que possuem um ciclo de vida na aplicação.

* Objetos de valores: objetos que somente carregam valores, mas sem identidade. Instâncias de objetos de valores são imutáveis.

* Agregados: classe agregadora de Entidades e Objetos de Valores. Serve para manter a integridade de seu modelo. Uma classe raiz é elencada e só se pode alterar o modelo a partir dessa classe.

* Fábricas - são classes usadas para a criação de agregados ou objetos de valores.

* Serviços - classes que possuem regras de negócio, mas que não pertencem as entidades, ou provém conexão entre entidades.

* Repositórios - administram o ciclo de vida de outros objetos. Centralizam as operações de criação, alteração e remoção de objetos.

* Módulos - agrupam classes por um determinado conceito de domínio.

## Exemplos de implementação

Apresentação de um exemplo de projeto usando as metodologias e patterns aplicados no DDD.

[Aurora API Project](https://github.com/alexalvess/aurora-api-project)

## Considerações finais

https://www.submarino.com.br/produto/130779534/livro-domain-driven-design-atacando-as-complexidades-no-coracao-do-software?pfm_carac=eric%20evans%20domain%20driven%20design&pfm_page=search&pfm_pos=grid&pfm_type=search_page

https://www.domainlanguage.com/ddd/

https://martinfowler.com/bliki/DomainDrivenDesign.html

http://www.macoratti.net/11/05/ddd_liv1.htm
