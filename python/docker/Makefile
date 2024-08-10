
command-list:
	@echo "command-list:"
	@echo " make build             - docker-compose build"
	@echo " make build-up          - docker-compose up -d --build"
	@echo " make nbuild            - docker-compose build --no-cache"
	@echo " make up                - docker-compose up -d"
	@echo " make down              - docker-compose down"
	@echo " make init-build-up     - docker-compose -f docker-compose.init.yml up -d --build"
	@echo " make init-nbuild       - docker-compose -f docker-compose.init.yml build --no-cache"
	@echo " make init-up           - docker-compose -f docker-compose.init.yml up -d"
	@echo " make vdown             - docker-compose down -v"


# Docker commands
build:
	docker-compose build

build-up:
	docker-compose up -d --build

nbuild:
	docker-compose build --no-cache

up:
	docker-compose up -d

down:
	docker-compose down

app:
	docker-compose exec python bash

app-www-data:
	docker-compose exec --user=www-data python  bash

vdown:
	docker-compose down -v
