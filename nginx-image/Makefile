build_run_webserver:
	containerId=$$(docker ps -aqf "name=webserver"); \
	if [ -n "$$containerId" ]; then \
	  docker container stop "$$containerId"; \
	  docker rm "$$containerId"; \
	  echo "Container stopped and removed."; \
	fi
	docker build -t nginx:1.0 .
	docker run -d -p 9090:80 --name webserver nginx:1.0