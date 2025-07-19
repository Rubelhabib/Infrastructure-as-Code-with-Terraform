# Terraform Commands Cheat Sheet

A quick reference of all important Terraform commands along with their English explanations.

---

## 🚀 Basic Commands

| Command             | Description                                               |
| ------------------- | --------------------------------------------------------- |
| `terraform init`    | Initializes the project. Downloads providers and modules. |
| `terraform plan`    | Shows what changes will be made. Does not apply them.     |
| `terraform apply`   | Applies the code and creates/updates the infrastructure.  |
| `terraform destroy` | Deletes all the created resources.                        |

---

## 🔍 Code Validation and Formatting

| Command              | Description                                |
| -------------------- | ------------------------------------------ |
| `terraform validate` | Checks for syntax or configuration errors. |
| `terraform fmt`      | Formats the code in standard style.        |
| `terraform show`     | Displays the current state data.           |

---

## 📄 State Management

| Command                                | Description                                        |
| -------------------------------------- | -------------------------------------------------- |
| `terraform state list`                 | Lists all managed resources.                       |
| `terraform state show <resource_name>` | Shows detailed information of a specific resource. |
| `terraform refresh`                    | Syncs real-time state with the state file.         |

---

## 🧪 Advanced Usage

| Command                             | Description                                                        |
| ----------------------------------- | ------------------------------------------------------------------ |
| `terraform output`                  | Displays output values (e.g., IP address).                         |
| `terraform graph`                   | Generates a dependency graph of resources (DOT format).            |
| `terraform taint <resource>`        | Forces a resource to be destroyed and recreated on the next apply. |
| `terraform untaint <resource>`      | Removes the taint from a resource.                                 |
| `terraform import <type.name> <id>` | Brings externally created resources under Terraform management.    |

---

## 🧹 Running with Options

| Command                           | Description                                      |
| --------------------------------- | ------------------------------------------------ |
| `terraform apply -auto-approve`   | Applies changes without asking for confirmation. |
| `terraform destroy -auto-approve` | Destroys resources without confirmation.         |
| `terraform plan -out=tfplan`      | Saves the execution plan to a file.              |
| `terraform apply tfplan`          | Applies changes using the saved plan file.       |

---

## 📂 Essential Files

| File/Folder         | Purpose                                                |
| ------------------- | ------------------------------------------------------ |
| `.terraform/`       | Contains Terraform cache and downloaded provider data. |
| `terraform.tfstate` | Stores the current state of the infrastructure.        |
| `terraform.tfvars`  | File to define variable values.                        |
| `main.tf`           | Main configuration file where resources are defined.   |
| `variables.tf`      | Defines input variables.                               |
| `outputs.tf`        | Specifies which values to output after applying.       |

---

## 📁 Example Terraform Project Structure

```
terraform-project/
├── main.tf          # Main Terraform configuration
├── variables.tf     # Input variables
├── outputs.tf       # Output values
├── terraform.tfvars # Variable values (optional)
└── README.md        # Documentation
```

---

## ✅ Practical Tips

- Always double-check before running `terraform destroy`.
- Keep the `.tfstate` file safe – it’s the heart of your project.
- Avoid committing `.terraform/` and `.tfstate` to Git (use `.gitignore`).

---
