# 🔑 Kubernetes Dashboard Admin User (Cluster RBAC)

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

Creates a **ServiceAccount** for the Kubernetes Dashboard and binds it to the **`cluster-admin` ClusterRole** with a ClusterRoleBinding, for local lab access.

## 📁 File

`dashboard-admin-user.yml`
- ServiceAccount `admin-user` in `kubernetes-dashboard`
- ClusterRoleBinding `admin-user-binding` → `cluster-admin`

## 🚀 Usage

```bash
kubectl apply -f dashboard-admin-user.yml
kubectl -n kubernetes-dashboard create token admin-user
kubectl proxy
```

## ⚠️ Security note

`cluster-admin` grants full control of the cluster. Use this **only on local/lab clusters**. In shared or production clusters, create a read-only or namespace-scoped role instead.

---

## 👤 Author

**Abdur Rehman** · DevSecOps Engineer · Founder of [ARTechOps](https://artechops.com)

[LinkedIn](https://www.linkedin.com/in/muhamad-abdur-rehman-81777b366/) · [GitHub](https://github.com/abdur-rehman-tech) · [artechops.com](https://artechops.com)
