<h1>🚀 Sobre o desafio</h1>
<p>Nesse desafio, você desenvolverá uma nova aplicação, a GoMarketplace. Dessa vez é hora de você praticar o que você aprendeu até agora no React Native junto com o TypeScript, utilizando rotas, Async Storage e a Context API.</p>
<h3>Utilizando uma fake API</h3>
<p>Antes de tudo, para que você tenha os dados para exibir em tela, criamos um arquivo que você poderá utilizar como fake API para te prover esses dados.

Para isso, deixamos instalado no seu package.json uma dependência chamada json-server, e um arquivo chamado server.json que contém os dados para uma rota /products. Para executar esse servidor você pode executar o seguinte comando:</p>
<pre>yarn json-server server.json -p 3333</pre>
<h3>Layout da aplicação</h3>
<p>Essa aplicação possui um layout que você pode seguir para conseguir visualizar o seu funcionamento.

O layout pode ser acessado através da página do Figma, no seguinte <a href="https://www.figma.com/file/VgK3hsmyGbqiGu9FdqfUzF/GoMarketplace">link</a>.

Você precisará de uma conta (gratuita) no Figma pra inspecionar o layout e obter detalhes de cores, tamanhos, etc.</p>
<h3>Funcionalidades da aplicação</h3>
<p>Agora que você já está com o template clonado e pronto para continuar, você deve verificar os arquivos da pasta src e completar onde não possui código, com o código para atingir os objetivos de cada rota.</p>
<ul>
<li>
<p><strong>Adicionar itens ao carrinho:</strong> Em toda sua aplicação, você deve utilizar o Contexto chamado cart que deixamos disponível. Você vai precisar completar as funcionalidades dentro de hooks/cart.tsx para que você consiga adicionar itens ao carrinho.</p>
</li><br>
<p><strong>Dica1:</strong> No seu contexto de carrinho, utilize uma propriedade chamada quantity para controlar quantos desse item existem no seu carrinho.</p>
<p><strong>Dica2:</strong> Caso um produto que você está adicionando já exista no carrinho, apenas altere a quantidade dele no seu contexto para evitar itens duplicados.</p>
<li>
<p><strong>Exibir itens do carrinho:</strong> Na página Cart você deve exibir todos os itens do carrinho, junto com a quantidade, valor único, valor subtotal dos itens e total de todos os items.</p>
</li>
<li>
<p><strong>Exibir itens do carrinho:</strong> Na página Cart você deve exibir todos os itens do carrinho, junto com a quantidade, valor único, valor subtotal dos itens e total de todos os items.</p>
</li>
<li>
<p><strong>Aumentar quantidade de itens do carrinho:</strong> Na página Cart você deve permitir que o usuário aumente a quantidade de itens do mesmo produto, para isso você pode utilizar a função increment dentro do seu contexto em /src/hooks/cart.tsx.</p>
</li>
<li>
<p><strong>Diminuir quantidade de um item do carrinho:</strong> Na página Cart você deve permitir que o usuário decremente a quantidade de itens do mesmo produto, para isso você pode utilizar a função decrement dentro do seu contexto em /src/hooks/cart.tsx.</p>
</li>
<li>
<p><strong>Exibir valor total dos itens no carrinho:</strong> Tanto na página Dashboard, quanto na página Cart você deve exibir o valor total de todos os itens que estão no seu carrinho.</p>
</li>
</ul>
<h3>Específicação dos testes</h3>
<p>Em cada teste, tem uma breve descrição do que sua aplicação deve cumprir para que o teste passe.</p>
<p>Para esse desafio, temos os seguintes testes:</p>
<ul>
<li>
<strong>should be able to list the products:</strong> Para que esse teste passe, sua aplicação deve permitir que sejam listados na sua tela Dashboard, todos os produtos que são retornadas do Fake API. Essa listagem deve exibir o title e o price que deve ser formatado utilizando a função Intl.
</li>
<li>
<strong>should be able to add a product to the cart:</strong> Para que esse teste passe, você deve permitir que seja possível adicionar produtos da sua Dashboard ao carrinho, utilizando o contexto de cart disponibilizado.
</li>
<li>
<strong>should be able to list the products on the cart:</strong> Para que esse teste passe, você deve permitir que seja possível listar os produtos que estão salvos no contexto do seu carrinho na página Cart, nessa página exiba o nome do produto e o subtotal total de cada produto (price * quantity).
</li>
<li>
<strong>should be able to calculate the cart total:</strong> Para que esse teste passe, tanto na página Dashboard, tanto na página Cart você deve exibir o valor total de todos os itens que estão no seu carrinho.
</li><br>
<p><strong>Dica:</strong> Para calcular o total de todos os itens, você pode utilizar o reduce para somar todos os valores e retornar o valor total.</p>
<li>
should be able to show the total quantity of itens in the cart: Para que esse teste passe, tanto na página Dashboard, tanto na página Cart você deve exibir o número total de itens que estão no seu carrinho.
</li><br>
<p><strong>Dica1:</strong> Para calcular o total de todos os itens, você pode utilizar o reduce para somar todos os valores e retornar o valor total.</p>
<p><strong>Dica2:</strong> Utilize o useMemo para armazenar o valor total do carrinho que você calculou.</p>
<li><br>
<strong>should be able to increment product quantity on the cart:</strong> Para que esse teste passe, você deve permitir que seja possível incrementar a quantidade de um produto do seu carrinho, utilizando o contexto de cart disponibilizado.
</li>
<li>
<strong>should be able to decrement product quantity on the cart:</strong> Para que esse teste passe, você deve permitir que seja possível decrementar a quantidade de um produto do seu carrinho, utilizando o contexto de cart disponibilizado.
</li><br>
<p><strong>Dica:</strong> Ao decrementar a quantidade de um produto, não permita que ele seja decrementado para um valor negativo, sendo a quantidade mínima 1 para estar no carrinho.</p>
<li>
<strong>should be able to navigate to the cart:</strong> Para que esse teste passe, no seu componente FloatingCart na Dashboard, você deve permitir que ao clicar no botão de carrinho com o testID de navigate-to-cart-button, o usuário seja redirecionado para a página Cart.
</li>
<li>
<strong>should be able to add products to the cart:</strong> Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que a função addToCart adicione um novo item ao carrinho.
</li>
<li>
<strong>should be able to increment quantity:</strong> Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que a função increment incremente em 1 unidade a quantidade de um item que está armazenado no contexto.
</li>
<li>
<strong>should be able to decrement quantity:</strong> Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que a função decrement decremente em 1 unidade a quantidade de um item que está armazenado no contexto.
</li>
<li>
<strong>should store products in AsyncStorage while adding, incrementing and decrementing:</strong> Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho você deve permitir que todas as atualizações que você fizer no carrinho, sejam salvas no AsyncStorage. Por exemplo, ao adicionar um item ao carrinho, adicione-o também no AsyncStorage. Lembre de também atualizar o valor do AsyncStorage quando você incrementar ou decrementar a quantidade de um item.
</li>
<li>
<strong>should load products from AsyncStorage:</strong> Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que todos os produtos que foram adicionados sejam buscados do AsyncStorage.
</li>
</ul>
