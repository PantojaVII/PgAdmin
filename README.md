# Projeto com pgAdmin no Docker

Este projeto configura um contêiner Docker para o pgAdmin4, uma interface gráfica de administração para bancos de dados PostgreSQL. O pgAdmin permite gerenciar e interagir com seu banco de dados de maneira fácil e intuitiva.

## 🚀 Como Rodar o Projeto
### 1. Pré-requisitos
Ter o Docker e o Docker Compose instalados em sua máquina.
Variáveis de ambiente configuradas:
- `PGADMIN_DEFAULT_EMAIL`: Email do usuário administrador do pgAdmin.
- `PGADMIN_DEFAULT_PASSWORD`: Senha do usuário administrador do pgAdmin.
- `PGADMIN_PORT`: Porta que o pgAdmin irá usar no seu sistema.
### 2. Configuração das Variáveis de Ambiente
Antes de rodar o Docker Compose, crie um arquivo .env no mesmo diretório do docker-compose.yml e defina as variáveis necessárias:


```
PGADMIN_DEFAULT_EMAIL=seuemail@dominio.com
PGADMIN_DEFAULT_PASSWORD=sua_senha_forte
PGADMIN_PORT=8080  # Exemplo de porta, altere conforme sua necessidade
```

### 3. Iniciar o Projeto
Com as variáveis de ambiente configuradas, inicie os serviços do Docker Compose com o seguinte comando:

```sh
docker-compose up -d
```

Este comando fará o seguinte:

- Subirá o serviço do pgAdmin, acessível na porta definida na variável PGADMIN_PORT (por padrão, a porta é 8080).
- Criará um volume persistente para os dados do pgAdmin (pgadmin_data).
- Conectará o pgAdmin à rede Docker nextcloud_cortex_network.

### 4. Acessando o pgAdmin
Após a execução do comando acima, você poderá acessar a interface web do pgAdmin através do navegador:

```
http://localhost:8080
```
