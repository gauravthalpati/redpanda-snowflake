# redpanda-snowflake
redpanda-snowflake using redpanda connect

To test the application, follow the below steps:

Step 1:
In your terminal, open the bash shell and start the Redpanda Connect stream by executing the below commands:

docker exec -it redpanda-0 /bin/bash

cd /tmp/campaign_analytics

rpk connect streams http_sf_stream.yaml


Step 2:
Open another terminal window and run the producer script that POSTs ad impressions and clicks for 5 different ads every 5 seconds. This script will stop after sending a total of 500 messages.

docker exec -it redpanda-0 /bin/bash

cd /tmp/campaign_analytics

sh produce_messages.sh


Step 3:
Open the Snowflake streamlit dashboard and view the dashboards in real-time. You can refresh it to see the updates in real time. 
Once the producer script is completed, you will see the final visualizations in the dashboard

