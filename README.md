# 🚀 Deploy Storage Account to Azure

This repository allows you to **automatically deploy** an **Azure Resource Group** and an **Azure Storage Account** using a **Deploy to Azure** button.

👉 No mandatory parameters are required: **resource names are generated automatically**.

---

## 📦 Deployed resources

The ARM template deploys:

* ✅ 1 **Resource Group** (auto-generated name)
* ✅ 1 **Storage Account** (`StorageV2`)
* ✅ SKU: `Standard_LRS`
* ✅ Access tier: `Hot`
* ✅ **Public Blob Access enabled**
* ✅ HTTPS traffic only

---

## 🧠 Automatic name generation

Names are generated using the Azure **subscription ID** to ensure global uniqueness.

* **Resource Group name**:

  ```text
  rg-storage-<hash>
  ```

* **Storage Account name**:

  ```text
  st<hash>
  ```

➡️ Re-deploying the template in the same subscription will result in the **same resource names**.

---

## ▶️ Deploy now

Click the button below to start the deployment:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjcabeza%2Fdeploy-to-azure%2Fmain%2Fazuredeploy.json)

### User steps

1. Sign in to the Azure Portal
2. Select the **subscription**
3. Click **Deploy**
4. Resources are created automatically

---

## 📄 Main file

* `azuredeploy.json` → ARM template (subscription-level deployment)

---

💡 *Feel free to fork this repository and adapt the deployment to your needs.*
