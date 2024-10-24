# Zabbix com Docker Compose e MySQL

Este projeto configura uma stack do Zabbix utilizando Docker Compose, com o banco de dados MySQL como backend. A stack inclui o servidor Zabbix, a interface web, Grafana e agentes para monitorar diferentes serviços.

## Pré-requisitos

- Docker
- Docker Compose

## Estrutura do Projeto

```plaintext
.
├── docker-compose.yml
└── zabbix
    ├── zabbix-mysql
    └── zabbix-server-module
```

## Configuração

### 1. Clonar o Repositório

Se você ainda não fez, clone o repositório:

```bash
git clone <URL_DO_REPOSITORIO>
cd <DIRETORIO_DO_REPOSITORIO>
```

### 2. Criar Diretórios

Crie os diretórios necessários para os volumes:

```bash
mkdir -p ./zabbix/zabbix-mysql
mkdir -p ./zabbix/zabbix-server-module
```

### 3. Configuração do Docker Compose

O arquivo `docker-compose.yml` contém a configuração para todos os serviços. Ele inclui:

- **zabbix-mysql**: Banco de dados MySQL 8.
- **zabbix-server**: Servidor Zabbix.
- **zabbix-frontend**: Interface web do Zabbix.
- **grafana**: Ferramenta de visualização.
- **Agentes Zabbix**: Para monitorar os serviços.

### 4. Executar os Serviços

Para iniciar todos os serviços, execute:

```bash
docker-compose up -d
```

### 5. Acessar a Interface do Zabbix

Acesse a interface web do Zabbix em [http://localhost:80](http://localhost:80). As credenciais padrão são:

- **Usuário**: Admin
- **Senha**: zabbix

## Adicionar Hosts

Para monitorar novos hosts:

1. Faça login na interface do Zabbix.
2. Vá para **Configuration** > **Hosts**.
3. Clique em **Create host** e preencha os detalhes.

## Parar os Serviços

Para parar e remover os contêineres, execute:

```bash
docker-compose down
```

## Contribuições

Sinta-se à vontade para contribuir! Abra um pull request ou issue se tiver sugestões ou melhorias.

## Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

---

Sinta-se à vontade para modificar qualquer seção para melhor atender às suas necessidades!
