TAG ?= 1.0.0
REPOSITORY ?= caiocezart

.SILENT:

.PHONY: build
build:
	docker-compose build app
	docker tag app:latest $(REPOSITORY)/app:$(TAG)

.PHONY: push
push:
	docker push $(REPOSITORY)/app:$(TAG)

.PHONY: deploy
deploy: build push

.PHONY: run
run:
	docker-compose up
