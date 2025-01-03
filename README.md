# Projeto-CookFood
Projeto Arquitetural de Software
## Discentes: Jéssica Cavalgante, João Victor Saraiva, Eduardo Felipe
## Docente: Fabrício Schlag
### Objetivos
* Descrever o escopo do sistema.
* Apresentar uma visão detalhada dos requisitos funcionais.
* Apresentar uma visão detalhada dos requisitos não funcionais.
* Descrever os principais casos de uso.
* Definir as interações dos usuários com o sistema.
* Definir a arquitetura do sistema.

## Público alvo
O CookFood é projetado para atender diferentes perfis de usuários apaixonados por culinária. O
sistema é ideal para cozinheiros amadores e entusiastas que buscam inspiração para novas
receitas ou desejam compartilhar suas próprias criações. Ele também atrai profissionais da área
gastronômica, como chefs e estudantes de gastronomia, que podem usar a plataforma para
descobrir novas receitas e compartilhar seu conhecimento.
Além disso, o CookFood atende pessoas que procuram receitas específicas, seja por preferências
alimentares, dietas, restrições ou até mesmo pela necessidade de preparar algo com os
ingredientes que já têm em casa. A plataforma também é uma excelente ferramenta para
blogueiros e criadores de conteúdo culinário, que podem compartilhar receitas e conectar-se com
uma comunidade de apaixonados por gastronomia.

## Descrição do sistema
O CookFood é uma plataforma online que oferece um catálogo de receitas, permitindo que usuários acessem, compartilhem e gerenciem receitas de forma interativa e intuitiva. O sistema está inserido no mercado da gastronomia, atendendo tanto cozinheiros amadores quanto profissionais. Sua principal funcionalidade é proporcionar uma interface amigável e robusta para que os usuários explorem uma vasta gama de receitas categorizadas, além de criar e compartilhar suas próprias receitas com a comunidade.
O sistema abrange funcionalidades que facilitam a navegação, organização e personalização da experiência do usuário, além de possibilitar a interação social entre os membros da plataforma.

## Descrição dos interessados do sistema

![image](https://github.com/user-attachments/assets/581ddfa6-8d8e-4233-88df-e82668c30753)

## Objetivos e características esperadas

![image](https://github.com/user-attachments/assets/c99ebc66-0036-4b40-a53e-9f78f0db3de4)

## Requisitos Funcionais
* **_RF01 - Requisito Funcional de Usuário:_** O sistema deve permitir que os usuários se registrem com um e-mail válido, senha ou utilizando login por redes sociais.
* **_RF02 - Requisito Funcional de Busca:_** O sistema deve permitir que os usuários busquem receitas através de filtros como nome da receita, ingredientes, categoria (sobremesas, pratos principais, etc.), tempo de preparo e restrições alimentares.
* **_RF03 - Requisito Funcional de Visualização:_** O sistema deve exibir detalhes das receitas, incluindo lista de ingredientes, modo de preparo, tempo de cozimento, porções e uma imagem ilustrativa.
* **_RF04 - Requisito Funcional de Inclusão de Receita:_** O sistema deve permitir que os usuários cadastrados adicionem suas próprias receitas, fornecendo informações como título, ingredientes, modo de preparo, tempo de preparo e uma imagem.
* **_RF05 - Requisito Funcional de Avaliação:_** O sistema deve permitir que os usuários deixem comentários e avaliem receitas de outros usuários, com uma escala de 1 a 5 estrelas e façam
comentários.
* **_RF06 - Requisito Funcional de Personalização:_** O sistema deve permitir que o usuário personalize o seu perfil, informando os seus dados e preferências dentro da plataforma.
* **_RF07 - Requisito Funcional de Login:_** O sistema deve possibilitar o login de usuários cadastrados, com validação de credenciais e recuperação de senha.
* **_RF08 - Requisito Funcional de Compartilhamento:_** O sistema deve permitir que os usuários compartilhem receitas nas redes sociais ou por links diretos.

## Arquitetura do Sistema

Para o CookFood, iremos utilizar uma Arquitetura de Microserviços. Este modelo distribui a aplicação em múltiplos serviços pequenos e independentes, cada um com uma responsabilidade específica, que se comunicam por meio de APIs. Essa abordagem é ideal para sistemas como o CookFood devido à flexibilidade, escalabilidade e facilidade de manutenção que oferece.
A arquitetura de microserviços permite que cada componente, como o serviço de gerenciamento de receitas, o serviço de autenticação de usuários e o serviço de notificações, seja desenvolvido, implantado e escalado separadamente. Isso facilita a evolução do sistema e garante um desempenho consistente, mesmo com o crescimento do número de usuários ou de novas funcionalidades. Além disso, essa arquitetura favorece a integração de novas tecnologias ou atualizações sem interferir em toda a aplicação.

![image](https://github.com/user-attachments/assets/966725c0-a361-4251-aca9-f8bf2396fcd6)

## Padrões de Projeto
Os Padrões de Design são soluções gerais para problemas recorrentes no desenvolvimento de software. Eles são utilizados para organizar e estruturar o código de forma que ele seja reutilizável, escalável e fácil de manter. No projeto CookFood, adotaremos o padrão MVC (ModelView-Controller) como base para organizar a lógica de apresentação e interação com o usuário, promovendo uma separação clara entre dados, interface e controle. Além disso, essa estrutura será combinada com uma arquitetura de Microserviços, visando a modularidade e a independência entre componentes.
O padrão MVC é amplamente utilizado em desenvolvimento de software, especialmente em sistemas que possuem uma interface de usuário interativa. Ele organiza a aplicação em três componentes principais:

* **_Model (Modelo):_** Representa os dados e a lógica de negócios da aplicação. No CookFood, o Model incluirá entidades como Receitas, Usuários, Categorias, e Comentários. Ele é responsável por acessar e manipular os dados, garantindo que as operações realizadas sobre eles respeitem as regras do sistema.

* **_View (Visão):_** Define a interface do usuário, apresentando as informações e interações necessárias. As Views no CookFood serão as páginas e componentes visuais onde os usuários poderão buscar e visualizar receitas, criar novas receitas e interagir com o conteúdo.

* **_Controller (Controlador):_** Serve como intermediário entre o Model e a View, controlando o fluxo de dados. No CookFood, os Controllers receberão as ações dos usuários (como buscar uma receita ou criar uma nova), interagirão com o Model para manipular os dados e, finalmente, atualizarão a View para exibir os resultados.

Dentro de cada microserviços, o padrão MVC organizará a lógica interna do serviço. Por exemplo, no Serviço de Receitas, o Model será responsável pela manipulação dos dados de receitas, o Controller cuidará das requisições que chegam (como busca e criação de novas receitas), e a View (quando aplicável, como uma API ou página específica) será responsável por retornar a resposta para o usuário ou para outro serviço.
Ao combinar MVC e Microserviços, o CookFood ganha uma estrutura robusta e eficiente para o desenvolvimento de suas funcionalidades. O padrão MVC organiza o código interno de cada microserviços, enquanto a arquitetura de microserviços garante flexibilidade e independência entre os módulos. Dessa forma, conseguimos um sistema que é tanto escalável quanto fácil de evoluir, adaptando-se rapidamente às novas necessidades dos usuários e exigências do mercado.

![image](https://github.com/user-attachments/assets/97b5c10e-7e8b-44a9-9fee-09da312c5517)

### Desenvolvimento de Microserviços
Cada microserviços será desenvolvido com foco na independência e responsabilidade única.

1. **Microserviços de Autenticação:** 
- Gerenciar o registro e login de usuários, utilizando _JWT_ para autenticação segura.
- Comunicação síncrona com o gateway API e comunicação assíncrona com outros
microserviços.

2. **Microserviços de Receitas:**
- CRUD de receitas. 
- Integração com o microserviços de buscas para indexação de novos dados.

3. **Microserviços de Avaliação e Comentários:**
- Gerenciar avaliações e comentários relacionados às receitas.
- Comunicação com o microserviços de receitas para exibição de avaliações médias. 

4. **Microserviços de Busca:** 
- Implementação com ElasticSearch para buscas rápidas e filtragem eficiente. 
- Atualização assíncrona por mensagens recebidas de outros microserviços.

## Destaques Técnicos
* Conformidade com LGPD para proteção de dados dos usuários.
* Design responsivo e acessível, atendendo padrões WCAG 2.1 AA.
* Desempenho otimizado para até 500 usuários simultâneos.

**_Contribuições são bem-vindas! Sinta-se à vontade!_** 🙂












