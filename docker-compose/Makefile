RUNNER ?= docker-compose -f ./docker-compose.tf.yaml run --rm

.PHONY: wordpress
wordpress:
	docker-compose up

.PHONY: tf12
tf12:
	$(RUNNER) tf12 version

.PHONY: tf11
tf11:
	$(RUNNER) tf11 version
