# frontend-socialdevs-argocd-bootstrap

Repositorio **sólo** para registrar la aplicación `socialdevs-frontend` en Argo CD mediante Ansible.

## 🚀 Cómo usar

```bash
# 1) Clona el repo y entra
git clone https://github.com/<TU_USUARIO>/frontend-socialdevs-argocd-bootstrap.git
cd frontend-socialdevs-argocd-bootstrap

# 2) (opcional) ajusta variables en vars/main.yml

# 3) Lanza el playbook
ansible-playbook playbooks/deploy_socialdevs_app.yml
```

## 🔧 Requisitos

- `kubectl` configurado con acceso al clúster
- `ansible >= 2.10`

## 📂 Estructura del proyecto

```
frontend-socialdevs-argocd-bootstrap/
├── README.md
├── ansible.cfg
├── inventory/
│   └── hosts.ini
├── vars/
│   └── main.yml
├── templates/
│   └── bootstrap-application.yaml.j2
└── playbooks/
    └── deploy_socialdevs_app.yml
```

## ✅ Resultado esperado

Si todo va bien, verás en la salida:

```
NAME                   SYNC STATUS   HEALTH STATUS
socialdevs-frontend    Synced        Healthy
```

Esto indica que Argo CD ya rastrea `socialdevs-frontend` y sincroniza los cambios desde:

📦 `https://github.com/vhgalvez/socialdevs-gitops/apps/socialdevs-frontend`
