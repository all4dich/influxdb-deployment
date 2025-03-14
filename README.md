# influxdb-deployment
## How to deploy
1. Run 'docker compose up -d' in workspace

## What you have to do before starting InfluxDB service
1. Create or update these three files with appropriate credentials.
   * .env.influxdb2-admin-username
   * .env.influxdb2-admin-password
   * .env.influxdb2-admin-token
1. Specify the desired data and configuration directories for InfluxDB. These can be modified within the 'volumes:' section by adjusting the 'device:' path.
    ```
    volumes:
      influxdb2-data:
        driver: local
        driver_opts:
          type: none
          o: bind
          device: ./data/db-data
    ```