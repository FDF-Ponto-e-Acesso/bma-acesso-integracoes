# Integração Externa com API BMA Acesso (Refeitório)

Esta é a documentação técnica de referência para a integração de sistemas parceiros e coletores físicos com a API do portal de refeitórios do sistema **BMA Acesso**. A comunicação é realizada por meio de chamadas HTTP/REST seguras utilizando payloads no formato JSON.

Para utilizar a integração externa, é obrigatório que as requisições sejam feitas sob o protocolo **HTTPS** com suporte ao protocolo criptográfico **TLS (Transport Layer Security) na versão 1.2 ou superior**.

## Documentação da API

A documentação da API está disponível por meio da [Coleção do Postman](./BMA_Acesso_Integracao_Externa.postman_collection.json) incluída neste repositório. Ela contém as requisições, parâmetros, exemplos de uso e facilita a validação dos endpoints durante a integração.

### Importante:

* **Credenciais de Integração:** Para realizar as chamadas à API, será necessário possuir uma conta de empresa ativa no sistema BMA Acesso. Você precisará do **CNPJ** correspondente e de um **TokenApi (Chave de Acesso Secundária)** cadastrado para a empresa no portal administrativo.
* **Autenticação:** As requisições são protegidas e exigem a geração prévia de um token de acesso **JWT Bearer** através do endpoint de login. Este token expira em **60 minutos**, sendo necessária sua renovação periódica.
* **Monitoramento de Saúde (Health Check):** A API disponibiliza o endpoint anônimo `GET /api/v3/Health` para verificação de disponibilidade do serviço e conectividade com o banco de dados.
* **Manual Técnico:** Leia o [Manual da Integração](./MANUAL_INTEGRACAO_BMA.pdf) atentamente para compreender o fluxo detalhado das rotas, parâmetros aceitos, respostas de erro e especificações de payloads.
* **Ambiente de Testes:** Importe e configure a coleção do Postman [BMA_Acesso_Integracao_Externa.json](./BMA_Acesso_Integracao_Externa.json) para testar os endpoints de autenticação, importação de usuários corporativos e consulta de históricos de refeição.

Em caso de dúvidas, consulte o suporte técnico.
