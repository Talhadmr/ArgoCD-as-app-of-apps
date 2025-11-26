k3d cluster list

k3d cluster delete --all

ansible-playbook -i Ansible/inventory.ini Ansible/setup-cluster.yml



kubectl port-forward svc/argocd-server -n argocd 8080:443

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
