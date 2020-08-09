# step 1
Clone this repo

# step 2 - build and run docker containers
```bash
docker-compose up -d --build
```
waiting for it to finish it takes when running it first time

# step 3
Go inside the docker and run following command
```bash
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition=2.2.6 .
```
It will require username and password you can grab those from here https://marketplace.magento.com/customer/accessKeys/

# step 4 - install magento 2
```bash
php bin/magento setup:install \
--admin-firstname=Anuj \
--admin-lastname=Kaushal \
--admin-email=anujkaushal@gmail.com \
--admin-user=admin \
--admin-password='Unique_Password' \
--base-url=https://mage2.local.test:32812 \
--base-url-secure=https://mage2.local.test:32812 \
--backend-frontname=admin \
--db-host=db \
--db-name=magento \
--db-user=root \
--db-password=root \
--use-rewrites=1 \
--language=en_US \
--currency=USD \
--timezone=America/New_York \
--use-secure-admin=1 \
--admin-use-security-key=1 \
--session-save=files \
--use-sample-data
```
change the information as per your need

# step 5 - stop and start containers
```bash
docker-compose down
docker-compose up -d
```

Thats it.. happy coding.
