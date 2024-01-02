# PA: Produto e Apresentação

A RedHot é uma loja online criada por um grupo de estudantes da Licenciatura em Engenharia Informática e Computação na FEUP, como projeto da UC LBAW. O objetivo principal é fornecer uma plataforma, sob a forma de *website*, dedicada à venda de produtos relacionados com malaguetas e picantes, abrangendo de utensílios e sementes para cultivo próprio a uma vasta gama de produtos picantes de diversas marcas, incluindo uma fictícia marca própria.

## A9: Produto

O artefacto a que o presente documeto está associado corresponde ao produto final desenvolvido pelo Grupo 2352 em LBAW.

Trata-se da Loja _Online_ RedHot: "A melhor loja de picantes do mundo", focada na temática dos produtos picantes (condimentos, sementes, etc.).

### 1. Instalação

O código-fonte do produto encontra-se em [git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/PA?ref_type=tags](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/PA?ref_type=tags) (_tag_ PA).

Para correr a imagem disponível no Registo de Contentores do GitLab (_GitLab Container Registry_), recorrendo à base de dados de produção, pode ser usado o seguinte comando _Docker_:

```shell
docker run -it -p 8000:80 --name=lbaw2352 -e DB_DATABASE="lbaw2352" -e DB_SCHEMA="lbaw2352" -e DB_USERNAME="lbaw2352" -e DB_PASSWORD="TPjjIRia" git.fe.up.pt:5050/lbaw/lbaw2324/lbaw2352
```

### 2. Uso

URL para o produto: http://lbaw2352.lbaw.fe.up.pt

#### 2.1. Credenciais de Administração

O URL para Administração é https://lbaw2352.lbaw.fe.up.pt/admin. No entanto, um administrador deve autenticar-se no _site_ da mesma maneira que um utilizador, ou seja, através de https://lbaw2352.lbaw.fe.up.pt/login. Após uma autenticação bem-sucedida, será, então, levado à página de administração com o URL referido.

| E-mail | Palavra-passe |
| ------ | ------------- |
| admin@admin.pt | 12345678 |

#### 2.2. Credenciais de Utilizador

| E-mail | Palavra-passe |
| ------ | ------------- |
| user@users.com | 12345678 |

### 3. Ajuda da Aplicação

A ajuda da RedHot reside na disponibilização de uma página de FAQs, de acesso livre, que pode ser modificada pelos administradores. Além disso, através da validação de _input_ do utilizador, são apresentadas mensagens de erro que ajudam os utilizadores a preencher corretamente os formulários, conforme abordado no tópico 2.2. Ainda, ações, como adição de um produto ao carrinho de compras, são acompanhadas por uma confirmação temporária (_pop-up_).

#### Página de FAQs

Na imagem abaixo, pode ser vista a referida página de perguntas frequentes e respetivas respostas, que ajudam os utilizadores a compreender a utilização do _website_, bem como políticas e regras da RedHot:

![FAQs](uploads/900c004a9c9e83efae8f2607dbb4da67/FAQs.png)

#### Adição de produto ao carrinho

A imagem que se segue denota um alerta de confirmação que é mostrado a um utilizador quando o mesmo adiciona um produto ao seu carrinho de compras:

![Carrinho_adicionar](uploads/c6bcb67c119b921b804c4b3e9b261ba4/Carrinho_adicionar.png)

### 4. Validação de _Input_

#### Lado do cliente

A validação de _input_ do lado do cliente reside nas propriedades dos elementos de formulário HTML. Esta abordagem evita pedidos desnecessários ao servidor, ao permitir que sejam acautelados, por exemplo, casos em que o utilizador deixa campos por preencher, introduz algo fora do devido formato, ou, ainda, valores numéricos fora dos limites definidos.

Segue-se um exemplo em que um utilizador autenticado tenta proceder ao _checkout_ do seu carrinho de compras, submetendo um número de cartão bancário para pagamento num formato inválido:

![erro_cartao](uploads/8162fb76a6bba6282545b776f37c16f7/erro_cartao.png)

#### Lado do servidor

Por sua vez, o servidor é responsável por validar a consistência de dados introduzidos, na medida em que seja necessário comparar valores, algo, portanto, além da mera verificação de formato do lado do cliente.

Abaixo, na imagem, encontra-se um exemplo em que um utilizador autenticado tenta alterar a sua palavra-passe, cometendo um erro na introdução da palavra-passe atual:

![erro_pass](uploads/7a010865ebf8a3eb67a31b8500a6ff7d/erro_pass.png)

### 5. Acessibilidade e Usabilidade

| _Checklist_ | Pontuação | Documento |
| ----------- | --------- | --------- |
| Acessibilidade | 16/18 | [```Acessibilidade.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/Checklists%20SAPO/Acessibilidade.pdf) |
| Usabilidade | 23/28 | [```Usabilidade.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/Checklists%20SAPO/Usabilidade.pdf) |

### 6. Validação de HTML e CSS

#### HTML

| Página validada | Documento |
| --------------- | --------- |
| Catálogo de Produtos (https://lbaw2352.lbaw.fe.up.pt/products) | [```products_html.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/HTML%20CSS%20valid/products_html.pdf) |
| _Dashboard_ de Administração (https://lbaw2352.lbaw.fe.up.pt/admin) | [```dashboard_html.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/HTML%20CSS%20valid/dashboard_html.pdf) |
| Página de Perfil de Utilizador (https://lbaw2352.lbaw.fe.up.pt/admin) | [```profile_html.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/HTML%20CSS%20valid/profile_html.pdf) |

#### CSS

| Ficheiro validado | Documento |
| ----------------- | --------- |
| ```products.css``` | [```products_css.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/HTML%20CSS%20valid/products_css.pdf) |
| ```admin.css``` | [```admin_css.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/HTML%20CSS%20valid/admin_css.pdf) |
| ```profile.css``` | [```profile_css.pdf``` no Repositório](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/HTML%20CSS%20valid/profile_css.pdf) |

### 7. Revisões ao Projeto

#### 7.1. A2: Atores e _User Stories_

- Antiga US005 deixa de ter prioridade "Alta" para passar a ser de prioridade "Média", trocando de posição e passando a ser US006. Aplicada a convenção Verbo + Objeto (por exemplo "Comprar Produto") aos nomes de todas as _User Stories_.
- Restrição C1: Alteração do prazo para que o sistema se encontre funcional.
- Adição da US006 (Constituição de carrinho de compras por utilizadores não autenticado) e consequente re-numeração das US seguintes na Tabela 2 (USs de Utilizador).
- Adição da US306 (Gestão de Encomentas) e consequente re-numeração das US seguintes na Tabela 5 (USs de Administrador).
- Adição da US110 (Receber notificações) e consequente da re-nomeação da antiga US110 para US111.
- Adição da US310 (Promover/despromover utilizador).
- Adição da US112 (Personalizar Perfil de Utilizador).
- Adição da US311 (Personalizar Perfil de Administrador).
- Adição da US113 (Recuperar palavra-passe).
- Adição da US011 (Ver produtos semelhantes).
- Adição da US012 (Ver data e hora de comentário).
- Adição da US013 (Ver produtos semelhantes no carrinho).
- Adição da US014 (Ver produtos semelhantes por categoria).
- Adição da US114 (Utilizar códigos promocionais).
- Adição da US311 (Personalizar Perfil de Administrador).
- Adição da US312 (Normalizar IDs de Produtos e Encomendas).
- Adição da US313 (Gerir de Códigos Promocionais).
- Adição da US314 (Visualizar Estatísticas de Visualização de Produtos).
- Adição da US315 (Monitorizar Carrinhos Ativos).

#### 7.2. A5 e A6 (Especificação da Base de Dados)

- Tabela ```Utilizador```
    - Adição dos atributos ```telefone```, ```morada```, ```codigo_postal```, ```localidade```, ```profile_image```, ```banned``` e ```became_admin```;
    - Adição do atributo ```banned``` para que, quando um utilizador registado decidir apagar os seus dados, a linha na tabela não ser completamente apagada, o que causaria erros em linhas de outras tabelas com _foreign keys_ que a referissem.
- Tabela ```Administrador```:
    - Adição do atributo ```profile_image```.
- Criação da tabela ```Promo_Codes```, para permitir a implementação de códigos promocionais para compras na RedHot.
- Tabela ```Compra```:
    - Adição dos atributos ```id_promo_code```, ```sub_total```, ```first_name```, ```last_name```, ```email```, ```telefone```, ```morada```, ```porta```, ```andar```, ```codigo_postal```, ```localidade```, ```pais```, ```nif``` e ```metodo_pagamento```.
- Tabela ```Notificacao```:
    - Adição dos atributos ```link```, ```lida``` e ```para_todos_administradores```.
- Tabela ```Produto```:
    - Adição dos atributos ```product_image```, ```categoria```, ```destaque``` e ```deleted```.
- Tabela ```Comentário```:
    - Adição do atributo ```editado```.
- Tabela ```ProdutoCarrinho```:
    - Adição do atributo ```timestamp```.
- Criação da tabela ```Faqs```, para permitir a implementação de perguntas frequentes (e respetivas respostas) sobre o funcionamento da RedHot.
- Criação da tabela ```Visits```, que possibilita contabilizar as visitas ao _website_, informação que consta dos dados estatísticos apresentados aos administradores.

### 8. Detalhes da Implementação

#### 8.1. Bibliotecas Usadas

| Nome | Descrição do uso | Exemplo |
| ---- | ---------------- | ------- |
| Chart.js | Para apresentar gráficos estatísticos ao administrador. | https://lbaw2352.lbaw.fe.up.pt/admin |
| Font Awesome | Para apresentar símbolos (p.ex. logo do LinkedIn). | https://lbaw2352.lbaw.fe.up.pt/about |
| SweetAlert2 | Pop-ups de confirmação (p.ex. eliminar produto). | https://lbaw2352.lbaw.fe.up.pt/products/1 (ao eliminar como administrador) |

#### 8.2 _User Stories_

| Módulo | Nome |
| ------ | ---- |
| M01 | Autenticação e Perfil |
| M02 | Produtos e Catálogo |
| M03 | Compras e Carrinho |
| M04 | Comentários e Avaliações |
| M05 | Páginas de administrador |
| M06 | Páginas estáticas |

| Identificador | Nome | Módulo | Prioridade | Membros da Equipa | Estado de Implementação |
| ------------- | ---- | ------ | ---------- | ----------------- | ----------------------- |
| US202 | Efetuar Registo | M01 | Alta | **Pedro Lima** | 100% |
| US201 | Efetuar _Log-in_ | M01 | Alta | **Pedro Lima** | 100% |
| US104 | Efetuar _Log-out_ | M01 | Alta | **Pedro Lima** | 100% |
| US001 | Visualizar Produto | M02 | Alta | **Pedro Landolt**, Pedro Lima | 100% |
| US002 | Visualizar Catálogo | M02 | Alta | **Pedro Landolt**, Pedro Lima | 100% |
| US003 | Pesquisar Produtos | M02 | Alta | **Pedro Lima**, Pedro Landolt | 100% |
| US004 | Filtrar por categoria | M02 | Alta | **Pedro Lima**, Pedro Landolt | 100% |
| US301 | Adicionar Produto | M02 | Alta | **Pedro Lima**, Pedro Januário | 100% |
| US302 | Alterar _stock_ | M02 | Alta | **Pedro Lima** | 100% |
| US303 | Remover Produto | M02 | Alta | **João Mota**, Pedro Januário | 100% |
| US005 | Visualizar Avaliações | M04 | Alta | **João Mota**, Pedro Landolt | 100% |
| US102 | Avaliar Produto | M04 | Alta | **João Mota**, Pedro Landolt | 100% |
| US107 | Editar Avaliação | M04 | Média | **João Mota**, Pedro Landolt | 100% |
| US108 | Eliminar Avaliação | M04 | Média | **João Mota** | 100% |
| US105 | Editar o perfil | M01 | Alta | **Pedro Januário**, Pedro Landolt, Pedro Lima | 100% |
| US109 | Eliminar Conta | M01 | Média | **Pedro Januário** | 100% |
| US101 | Comprar Produtos | M03 | Alta | **Pedro Januário** | 100% |
| US103 | Seguir Encomenda | M03 | Alta | **Pedro Januário**, Pedro Landolt | 100% |
| US106 | Cancelar Encomenda | M03 | Média | **Pedro Januário**, Pedro Lima | 100% |
| US306 | Gerir Encomendas | M03 | Alta | **Pedro Januário**, Pedro Lima | 100% |
| US304 | Consultar Estatísticas | M05 | Alta | **Pedro Landolt**, João Mota | 100% |
| US009 | Consultar a Política de Privacidade | M06 | Baixa | **Pedro Landolt** | 100% |
| US010 | Consultar os Termos de Utilização | M06 | Baixa | **Pedro Landolt** | 100% |
| US006 | Constituir Carrinho | M03 | Média | **Pedro Januário** | 100% |
| US113 | Recuperar palavra-passe | M01 | Baixa | **João Mota** | 100% |
| US111 | Constituir Lista de desejos | M02 | Baixa | **João Mota** | 100% |
| US008 | Consultar _Acerca de_ | M06 | Baixa | **Pedro Landolt** | 100% |
| US110 | Receber notificações | M01 | Média | **Pedro Lima** | 100% |
| US007 | Visualizar FAQs | M06 | Média | **Pedro Landolt** | 100% |
| US011 | Ver produtos semelhantes | M02 | Baixa | **Pedro Landolt** | 100% |
| US305 | Gerir FAQs | M06 | Alta | **Pedro Landolt**, João Mota | 100% |
| US307 | Gerir Destaques | M06 | Alta | **João Mota**, Pedro Landolt | 100% |
| US309 | Banir utilizador | M01 | Média | **Pedro Januário** | 100% |
| US310 | Promover/despromover utilizador | M01 | Média | **Pedro Januário** | 100% |
| US308 | Remover comentário | M04 | Média | **João Mota** | 100% |
| US311 | Personalizar Perfil de Administrador | M01 | Baixa | **Pedro Januário** | 100% |
| US011 | Ver produtos semelhantes | M02 | Baixa | **Pedro Landolt** | 100% |
| US012 | Ver data e hora de comentário | M04 | Baixa | **Pedro Landolt** | 100% |
| US013 | Ver produtos semelhantes no carrinho | M02 | Baixa | **Pedro Landolt** | 100% |
| US014 | Ver produtos semelhantes por categoria | M02 | Baixa | **Pedro Landolt** | 100% |
| US114 | Utilizar códigos promocionais | M03 | Baixa | **Pedro Landolt** | 100% |
| US311 | Personalizar Perfil de Administrador | M01 | Baixa | **Pedro Landolt** | 100% |
| US312 | Normalizar IDs de Produtos e Encomendas | M02 | Baixa | **Pedro Landolt** | 100% |
| US313 | Gerir Códigos Promocionais | M05 | Baixa | **Pedro Landolt** | 100% |
| US314 | Visualizar Estatísticas de Visualização de Produtos | M05 | Baixa | **Pedro Landolt** | 100% |
| US315 | Monitorizar Carrinhos Ativos | M05 | Baixa | **Pedro Landolt** | 100% |

## A10: Apresentação
 
O presente artefacto corresponde à apresentação do produto final desenvolvido pelo grupo.

### 1. Apresentação do Produto

A RedHot é "a melhor loja de picantes do mundo". Dedica-se aos produtos picantes, desde condimentos e molhos, a sementes para cultivo próprio. A RedHot oferece aos seus clientes a possibilidade de explorar e filtrar todo o catálogo de produtos, constituir um carrinho de compras e efetuar encomendas caso se autentiquem. Utilizadores registados podem, ainda, constituir uma lista de desejos, gerir as suas encomendas, editar o seu perfil e ser notificados de alterações às suas encomendas.

O _site_ contempla, ainda, a indispensável vertente de administração do mesmo. Administradores podem editar, adicionar ou mesmo eliminar produtos, bem como gerir FAQs, banir utilizadores ou promovê-los a administrador. E como dados concretos sobre a operação são indispensáveis para a gestão de qualquer negócio, os dados estatísticos mais recentes estão sempre disponíveis para consulta pelos administradores.

URL para o produto: http://lbaw2352.lbaw.fe.up.pt

### 2. Apresentação em vídeo

![Captura_de_ecrã_2023-12-21_205939](uploads/329a08c2171cd1ed5e9c8c9955ef6724/Captura_de_ecrã_2023-12-21_205939.png)

O vídeo completo encontra-se disponível no [repositório do grupo](https://git.fe.up.pt/lbaw/lbaw2324/lbaw2352/-/tree/main/docs/video/lbaw2352.mp4).

## Histórico de Revisões

N/A (primeira submissão)

---

GRUPO 2352, 21/12/2023

- João Guimarães Mota, up202108677@up.pt
- Pedro de Almeida Lima, up202108806@up.pt
- Pedro Jorge Mendes Jesus Landolt, up202103337@up.pt
- Pedro Simão Januário Vieira, up202108768@up.pt (editor)
