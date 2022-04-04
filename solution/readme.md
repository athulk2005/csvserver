Part 1
-------
1. Pull image : docker pull infracloudio/csvserver:latest

2. gencsv.sh : download the script attached in the solution folder. Execute - ' chmod 755 gencsv.sh ' to provide execute permission.
4. Docker command : docker run -d --name "csvserver" -v /home/athul/Documents/assessment/csvserver/solution/inputFile:/csvserver/inputdata infracloudio/csvserver:latest

5. Find app listening port : docker inspect csvserver
	: from the output, under "Config" block, look for exposed port number. : ExposedPorts

6. Stop and delete the container
	docker stop csvserver
	docker rm csvserver

7. Re- run with all arguments.  Docker command : docker run -d --name "csvserver" -v /home/athul/Documents/assessment/csvserver/solution/inputFile:/csvserver/inputdata -e CSVSERVER_BORDER=Orange -p 9393:9300 infracloudio/csvserver:latest

	Explanation: docker run -d --name "csvserver" -v <inputFile path of host>:/csvserver/inputdata -e CSVSERVER_BORDER=Orange -p 9393:9300 <container id>




