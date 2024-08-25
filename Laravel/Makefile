default:
	@echo "Available commands:"
	@echo "  make migrate        - Run migrations"
	@echo "  make mig-roll   - Rollback migrations"
	@echo "  make mig-status     - Show migration status"
	@echo "  make seed           - Run seeds"
	@echo "  make tinker         - Run tinker"
	@echo "  make test           - Run tests"
	@echo "  make config-clear   - Clear config cache"
	@echo "  make cache-clear    - Clear cache"
	@echo "  make m-mig         - Create migration"
	@echo "  make a-mig         - Create add column migration"
	@echo "  make c-mig         - Create change column migration"
	@echo "  make m-model        - Create model"
	@echo "  make m-model-mig    - Create model and migration"
	@echo "  make m-ctrl         - Create controller"
	@echo "  make m-rule         - Create rule"



# Laravel commands
migrate:
	php artisan migrate

mig-roll:
	php artisan migrate:rollback
mig-status:
	php artisan migrate:status

seed:
	php artisan db:seed

tinker:
	php artisan tinker

test:
	php artisan test

config-clear:
	php artisan config:clear

cache-clear:
	php artisan cache:clear


# Create migration with specified filename
m-mig:
	@read -p "Enter migration name: " name; \
	php artisan make:migration create_$${name}_table

a-mig:
	@read -p "Enter column name: " column; \
	read -p "Enter table name: " table; \
	php artisan make:migration add_$${column}_to_$${table}_table --table=$${table}

c-mig:
	@read -p "Enter column name: " column; \
	read -p "Enter table name: " table; \
	php artisan make:migration change_$${column}_in_$${table}_table --table=$${table}

# Create model with specified filename
m-model:
	@read -p "Enter model name: " name; \
	php artisan make:model $$name

m-model-mig:
	@read -p "Enter model name: " name; \
	php artisan make:model $$name -m

m-rule:
	@read -p "Enter rule name: " name; \
	php artisan make:rule $$name

# Create controller with specified filename
m-ctrl:
	@read -p "Enter controller name: " name; \
	php artisan make:controller $$name
