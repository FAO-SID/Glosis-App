# Glosis-App
Application for the GloSIS database creation and data injection from excel files (.xlsx).

**Installation**

To create a new installation of the app, downdload the 'docker-compose.yml' file to a folder in your computer. Within that folder, run the following command in your CMD (windows) or Terminal (mac/linux):

	docker-compose up --build -d


**Test data:**

Download the test data for testing the application.

Test data from:
Poels, R. L. H. 1987. “Soils, Water and Nutrients in a Forest Ecosystem in Suriname.” PhD thesis, Wageningen, Netherlands: Agricultural University, Wageningen.

**Remove the Application**

To remove all existing images, containers and databases, run the following commands in your docker-compose.yml folder

	docker stop $(docker ps -q)
	docker rm $(docker ps -aq)
	docker rmi $(docker images -q) --force
	docker network prune -f
	docker volume prune -f
	docker system prune -a --volumes -f
