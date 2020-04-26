.PHONY: mariadb
mariadb:
	docker run --name db -e MYSQL_ROOT_PASSWORD=example -d mariadb

.PHONY: app
app:
	docker run --name wordpress --link db:mysql -p 8080:80 -d wordpress

.PHONY: wordpress
wordpress: mariadb app

.PHONY: tf12
tf12:
	docker run --rm -it hashicorp/terraform:0.12.24 version

.PHONY: tf11
tf11:
	docker run --rm -it hashicorp/terraform:0.11.14 version

.PHONY: clean
clean:
	docker rm -f db
	docker rm -f wordpress
