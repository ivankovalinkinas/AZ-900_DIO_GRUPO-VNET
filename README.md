# 📘 Guia de Estudo - Certificação AZ-900


## 🏗️ Criando Recursos no Azure

Nesta prática vamos aprender a criar:
1. **Grupo de Recursos**  
2. **Rede Virtual (VNet)**  

Esses dois componentes são a base para hospedar soluções na nuvem.

---


## 📂 1. Criando um Grupo de Recursos

O **Grupo de Recursos** é como um "container lógico" onde ficam todos os recursos do Azure (VMs, redes, bancos, etc.). Com seu uso facilita a organição dos recursos por departamente, projeto, empresa, etc.

### Portal Azure (Interface gráfica)
1. Acesse o [Portal do Azure](https://portal.azure.com).
2. No Portal, pesquise por **Grupos de Recursos**.
3. Clique em **+ Criar**.
4. Preencha:
   - **Assinatura:** escolha sua assinatura do Azure.
   - **Grupo de Recursos:** defina um nome (ex: `RG-Estudo-AZ900`).
   - **Região:** escolha a mais adequada ao seu projeto (ex: `Brazil South`).
5. Clique em **Revisar + Criar** → **Criar** ✅

### Azure CLI (linha de comando)
```PowerShell
az group create --name RG-Estudo-AZ900 --location brazilsouth
```

---


## 🌐 2. Criando uma Rede Virtual (VNet)

A **Rede Virtual (VNet)** é como uma rede privada dentro do Azure, onde você conecta máquinas virtuais, bancos de dados e outros serviços.

### Portal Azure (Interface gráfica)
1. Acesse o [Portal do Azure](https://portal.azure.com).
2. No Portal, pesquise por **Rede Virtual**.
3. Clique em **+ Criar**.
4. Preencha:
   - **Grupo de Recursos:** ex: `RG-Estudo-AZ900` criado acima.
   - **Nome da VNet:** defina um nome (ex: `VNet-Estudo-AZ900`)
   - **Região:** escolha a mais adequada ao seu projeto (ex: `Brazil South`).
   - **Configure o Espaço de Endereços** (ex: `10.0.0.0/16`).
   - **Configure a Sub-rede** (ex: `10.0.1.0/24`).
5. Clique em **Revisar + Criar** → **Criar** ✅

### Azure CLI (linha de comando)
```PowerShell
az network vnet create --resource-group RG-Estudo-AZ900 --location brazilsouth --name VNet-Estudo-AZ900 --address-prefix 10.0.0.0/16 --subnet-name Subnet-Principal --subnet-prefix 10.0.1.0/24
```

---
