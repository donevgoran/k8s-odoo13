# Odoo ERP deployment for kubernetes

Before start, you need to build the docker image, or you can use the official image by odoo's, in my example i have my private build for a secure perspective

```bash
docker build -t odoo13 .
```

add a tag 

```bash
docker tag odoo13 dockerhub_username/odoo13
```
push the image to your dockerhub account

```bash
docker push dockerhub_username/odoo13
```
then you are ready to deploy the odoo to your kubernetes.

```bash
kubectl apply -f k8s-odoo.yaml
```
**PGSQL PASSWORD: password1!**

**Master PASSWORD: password1!**

**P.S. This example is used for DEV environment, is not tested in production**
