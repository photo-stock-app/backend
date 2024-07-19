start-dev:
	$(MAKE) down-dev
	docker-compose --env-file ../.env.local -p dev up --build

restart-dev:
	#docker context use default
	#$(MAKE) down-dev#
	docker-compose --env-file ../.env.local -p dev restart
down-dev:
	docker-compose -p dev down --rmi local --volumes --remove-orphans

clean-up:
	docker image prune -a -f
	docker volume prune -f
	docker system prune -f



