# Velero Demo

```bash
velero backup create nginx-demo --default-volumes-to-fs-backup --include-namespaces=default --wait
velero backup logs nginx-demo

velero restore create nginx-demo --from-backup nginx-demo
velero restore logs nginx-demo

velero restore delete nginx-demo
velero backup delete nginx-demo
```