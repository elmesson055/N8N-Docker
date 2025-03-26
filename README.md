# N8N Docker Setup

Automated workflow automation tool running in Docker with persistent storage.

## Pré-requisitos
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) instalado
- Drive compartilhado habilitado nas configurações do Docker (Settings -> Resources -> File Sharing)

## Configuração Inicial

1. **Criar arquivo de ambiente**:
   ```bash
   cd C:\Users\***********\Desktop\N8N-Docker
   notepad .env

   Adicione estas variáveis (altere USER e PASSWORD):

   DATA_PATH=C:\Users\************\Desktop\N8N-Docker\n8n-data


N8N_BASIC_AUTH_USER=seu_usuario
N8N_BASIC_AUTH_PASSWORD=sua_senha_forte
TZ=America/Sao_Paulo

2. Iniciar container

 docker-compose up -d


 ## Acessar Interface
- URL: http://localhost:5678
- Credenciais: Usuário/senha configurados no .env


## Persistência de Dados
- Todos os workflows são armazenados em:

C:\Users\***********\Desktop\N8N-Docker\n8n-data


Para resetar permissões (execute como Admin):

icacls "C:\Users\***********\Desktop\N8N-Docker\n8n-data" /grant:r "Everyone:(OI)(CI)F"

## Comandos Úteis Descrição Comando Parar container

docker-compose down Reiniciar com novas configurações

docker-compose up -d --force-recreate Ver logs

docker-compose logs -f
## Configurações Adicionais
- Alterar porta : Atualize ports no docker-compose.yml e a variável N8N_PORT no .env
- Time Zone : Edite a variável TZ no .env ( Lista de Time Zones )
## Segurança
- Mantenha o arquivo .env fora de sistemas de versão (adicionar ao .gitignore )
- Altere as credenciais padrão imediatamente após a primeira execução


Key features included:
1. Windows-compatible path instructions
2. Permission management commands
3. Table of essential commands
4. Security recommendations
5. Timezone configuration guidance
6. Persistent storage location details

Para atualizar o README após modificações, basta editar o arquivo e manter junto com sua configuração do Docker.