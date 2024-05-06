# Observações / Boas Práticas

- Split pela virgula, fazendo um replace para . não funciona no método pois não existe a virgula para fazer o replace, sendo que o split é feito em cima da virgula.

- Calcular o sub-total no método de executar a compra não é uma boa prática, pois o sub total deve ser gerado com base nos valores lidos (compras.txt) e não durante a leitura de cada item.

## Tipos de Testes que poderiam ser feitos

> [!IMPORTANT] 
> Precisa ter `Assert` para ser um teste

- Carrega Produto
```java
void carregaProdutoTest(){
	loja.carregaProdutos();
	assertFalse(loja.getProdutos().size() == 0);
	assertTrue(loja.getProdutos().size() == 50);
	assertEuals("Banana",loja.produtos().get(0).getNome());
}
```
- Total Compra

- Processar/Executar Compra
```java
void processaCompraTest(){
	loja.carregaProdutos();
	loja.carregaCompras();
	loja.processaCompra();
	assertEquals(new File("Compra.txt").exists());
	assertEquals(179.5,loja.getTotalCompra());
	
}
```

- Carrega Lista de Compras
```java
void carregaListaComprasTest(){
	loja.carregaProdutos();
	loja.carregaCompras();
	assertFalse(loja.getItens().size() == 0);
	assertTrue(loja.getItens().size() == 10);
	assertEuals("Maçã",loja.produtos().get(0).getProduto().getNome());
}
```



# Execções JAVA

- Condição Excepcional, ou seja, é um tratamento de algo esperado que possa ocorrer com determinada situação

- Classe Error: é um problema que não é possível tratar, semelhante a algo crítico.

- Tratamento de Exceção: Protege o código, do mais interno para o mais externo.

- Throw: Força uma execeção

- Throws: Expande a possibilidade de tratamento ao usuário final tratar. Mas é necessário tratar parcialmente antes de disponibilizar.

- Finally: é sempre executado, mesmo depois de executar um exception.



#  2a Avaliação POO

> [!TIP]
> O que vai cair na avaliação

- arquivo de estoque ou compra.
- ler uma tabela de banco de dados e exportar para arquivo

> [!IMPORTANT]  
> Deixar pronto algo que faça isso
> Deve possuir testes unitários




- Realizar os testes da atividade de perguntas e respostas
- Não vai cair a parte de properties
- Criar projetos e mapear no github
- Criar projetos de leitura e gravação de texto