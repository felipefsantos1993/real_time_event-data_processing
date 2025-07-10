# 🚀 Terraform para Azure Event Hub

## ✅ Pré-requisitos

- [Terraform instalado](https://developer.hashicorp.com/terraform/downloads)
- [Azure CLI instalado](https://learn.microsoft.com/pt-br/cli/azure/install-azure-cli)
- Conta no Azure com permissões para criar recursos

---

## 📁 Estrutura dos Arquivos

```
eventhub-terraform/
├── main.tf           # Recursos a serem criados
├── variables.tf      # Variáveis de entrada
├── outputs.tf        # Saídas (como a connection string)
```

---

## 🧭 Passo a Passo

### 1. 📂 Extraia o ZIP

```bash
unzip eventhub-terraform.zip
cd eventhub-terraform
```

---

### 2. 🔐 Faça login no Azure

```bash
az login
```

Se necessário, selecione sua assinatura:

```bash
az account set --subscription "ID-ou-nome-da-assinatura"
```

---

### 3. ⚙️ Inicialize o Terraform

```bash
terraform init
```

---

### 4. 👁️ Visualize o que será criado

```bash
terraform plan
```

---

### 5. 🚀 Aplique a infraestrutura

```bash
terraform apply
```

Digite `yes` quando solicitado.

---

### 6. 📤 Veja os outputs

Você verá os seguintes valores:

- Nome do namespace
- Nome do Event Hub
- Connection string da authorization rule (sensitive)

---

### 🧽 (Opcional) Destruir a infraestrutura

```bash
terraform destroy
```

---

## 📌 Observações

- O `namespace_name` precisa ser **único globalmente**.
- A connection string é necessária para que aplicativos enviem mensagens para o Event Hub.
- Você pode adaptar este projeto para múltiplos ambientes com arquivos `.tfvars`.

---

## 📄 Licença

Uso livre para fins educacionais e comerciais.