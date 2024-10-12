# Testes de API com Postman

Este repositório contém um conjunto de testes automatizados para uma API REST simples. Utilizei o Postman para criar, validar e realizar testes de performance, incluindo requisições **GET**, **POST**, **PUT** e **DELETE**. O objetivo é garantir a consistência das respostas e a performance da API.

## Tabela de Conteúdos

- [Descrição](#descrição)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Como Usar](#como-usar)
  - [Importar a Coleção no Postman](#importar-a-coleção-no-postman)
  - [Executar os Testes](#executar-os-testes)
- [Testes de Performance](#testes-de-performance)
- [Contribuindo](#contribuindo)

## Descrição

Este projeto foi desenvolvido para demonstrar o uso de testes de API automatizados utilizando o Postman, incluindo a validação de tempo de resposta com base em testes de performance. Ele abrange as operações principais de uma API REST:

- **GET**: Recuperar dados.
- **POST**: Criar novos dados.
- **PUT**: Atualizar dados existentes.
- **DELETE**: Excluir dados.

Além disso, são realizados testes para garantir que o tempo de resposta da API esteja dentro dos limites aceitáveis.

## Tecnologias Utilizadas

- [Postman](https://www.postman.com/)
- [Newman](https://github.com/postmanlabs/newman) (opcional para execução via CLI)

## Como Usar

### Importar a Coleção no Postman

1. Clone este repositório ou faça o download do arquivo `.postman_collection.json` para sua máquina.

   ```bash
   git clone https://github.com/seu-usuario/testes-api-postman.git
   ### Importar a Coleção no Postman
  
2. Abra o Postman e clique em **Import**.
3. Selecione o arquivo `.postman_collection.json` baixado.
4. Agora você verá a coleção com todas as requisições (GET, POST, PUT, DELETE) e os testes de performance configurados.

### Executar os Testes
1. Selecione a coleção importada no Postman.
2. Clique em **Run** para executar todos os testes de uma vez.
3. Verifique os resultados dos testes na aba **Test Results** para ver se as validações foram bem-sucedidas.

### Testes de Performance
Todos os testes de API incluem uma verificação de tempo de resposta para garantir que a API responda dentro de um limite aceitável. Por padrão, o tempo de resposta deve ser inferior a 200ms.

Aqui está um exemplo de código utilizado nos testes:
```javascript
pm.test("Response time is less than 200ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(200);
});

## Contribuindo
Sinta-se à vontade para abrir uma issue ou enviar um pull request caso queira sugerir melhorias ou correções.


