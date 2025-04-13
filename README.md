# ☁️ Configuração de Instância de Banco de Dados na Microsoft Azure

Este repositório documenta o processo de provisionamento e configuração de uma instância de banco de dados gerenciado na plataforma Microsoft Azure. O objetivo é demonstrar a criação, segurança e conexão a um banco de dados em nuvem, utilizando boas práticas de arquitetura e gerenciamento.

---

## 📌 Objetivo

Provisionar uma instância de banco de dados relacional na Azure, permitindo acesso seguro e remoto para administração e utilização em aplicações.

---

## 💻 Tecnologias Utilizadas

- **Plataforma:** Microsoft Azure
- **Banco de Dados:** SQL Server / MySQL / PostgreSQL 
- **Ferramentas de Conexão:** 
  - Azure Data Studio / SQL Server Management Studio (SSMS)
  - MySQL Workbench / pgAdmin *(dependendo do banco)*
- **Gerenciamento de IPs e Firewalls**
- **Azure Resource Groups & Pricing Tiers**

---

## ⚙️ Etapas de Configuração

### 1. Acesso à Azure

Acesse o portal: [https://portal.azure.com](https://portal.azure.com)

### 2. Criação do Recurso

- Navegue até **"Criar um recurso"** > Escolha o tipo de banco desejado.
- Exemplos: *SQL Database*, *Azure Database for MySQL*, *Azure Database for PostgreSQL*.

### 3. Parâmetros de Configuração

- **Assinatura**: Selecione a assinatura ativa.
- **Grupo de Recursos**: Utilize um existente ou crie um novo.
- **Nome da Instância**: Escolha um identificador único.
- **Servidor**: Crie um novo servidor definindo:
  - Nome do host
  - Nome de usuário e senha de administrador
  - Região (ex: Brazil South)
- **Camada de Serviço (Pricing Tier)**: Escolha conforme desempenho e custo estimado (ex: Basic, General Purpose, Business Critical).

### 4. Segurança e Acesso

- Acesse o recurso do **servidor**.
- Vá em **Firewalls e redes virtuais** e:
  - Adicione o endereço IP público do seu ambiente local.
  - Configure o acesso a redes seguras conforme necessário.

### 5. Conexão ao Banco

- Utilize a string de conexão fornecida no painel da Azure.
- Ferramentas recomendadas:
  - **SQL Server**: Azure Data Studio, SSMS
  - **MySQL**: MySQL Workbench
  - **PostgreSQL**: pgAdmin
- Teste a conexão com as credenciais definidas.

---

## ✅ Boas Práticas

- Utilizar **Azure Key Vault** para gerenciamento seguro de segredos e credenciais.
- Evitar exposição pública do banco de dados (manter acesso restrito por IP).
- Definir políticas de backup e alta disponibilidade.
- Monitorar desempenho com **Azure Monitor** e configurar alertas.
