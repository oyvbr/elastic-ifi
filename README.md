# Traffic accidents

### Download and install Docker: 
- Create a Docker account if you don't have one

- https://www.docker.com/get-started (for Windows and Mac)

- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04 (for Ubuntu)

Verify the installation by running `docker version` in terminal/PowerShell

### Run the Docker Image
- Run: `docker run --rm -p 5601:5601 -p 9200:9200 oyvindbratvedt/elastic-ifi:1` in terminal/PowerShell in order to start the Docker image.
- The image will start Elasticsearch, index the ~289000 traffic accidents, and start Kibana. Soon after the accidents are finished indexing, you can open Kibana in your browser. 
- Open Kibana in your browser on http://localhost:5601

### Configure Kibana
#### Set Index Pattern
- In Kibana, navigate to **Management** and click **Index Patterns**.
- Enter `accidents` in the **Index pattern** field. 
- Click **Next step**
- In **Configure settings**, select **timestamp** in the **Time Filter field name** dropdown menu.

#### Get data from further back than 15 minutes
- Navigate to **Discover**
- In the top right corner, press **Last 15 minutes**
- In the **Time Range** menu, press **Relative**
- Change the **From** field to 50 years ago
- Click **Go**
- Now you should see all the accidents in the dataset


### Kibana
Now you can play around with the data in Kibana. Go to **Visualize** where you can create coordinate maps, graphs and plots visualizing the accidents. 
