# Traffic accidents

### Download and install Docker: 
- Create a Docker account if you don't have one

- https://www.docker.com/get-started (for Windows and Mac). Windows users need Hyper-V in order to run Docker. This is automatically enabled when installing Docker Desktop on Windows. If you need to enable it manually, have a look at this link: https://docs.docker.com/machine/drivers/hyper-v/

- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04 (for Ubuntu)

Verify the installation by running `docker version` in terminal/PowerShell

### Run the Docker Image
- Run: `docker run --rm -p 5601:5601 -p 9200:9200 oyvindbratvedt/elastic-ifi` in terminal/PowerShell in order to start the Docker image.
- The image will start Elasticsearch., index the ~290000 traffic accidents, and start Kibana. You will see some errors in the console initially while it waits for Elasticsearch to be fully started. Soon after the accidents are finished indexing, you can open Kibana in your browser. 
- Open Kibana in your browser on http://localhost:5601

### Configure Kibana
#### Set Index Pattern
- In Kibana, navigate to **Management** and click **Index Patterns**.
- Enter `accidents` in the **Index pattern** field. 
- Click **Next step**
- In **Configure settings**, select **timestamp** in the **Time Filter field name** dropdown menu.
- Click **Create index pattern**

#### Get data from further back than 15 minutes
- Navigate to **Discover**
- In the top right corner, press **Last 15 minutes**
- In the **Time Range** menu, press **Relative**
- Change the **From** field to 50 years ago
- Click **Go**
- Now you should see all the 289610 accidents in the dataset 


### Kibana
Now you can play around with the data in Kibana. Go to **Visualize** where you can create coordinate maps, graphs and plots visualizing the accidents. 

# Tasks
https://github.com/oyvbr/elastic-ifi/blob/master/tasks.md
