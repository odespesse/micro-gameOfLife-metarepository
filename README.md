# micro-gameoflife-metarepository

1. Build each dependency individually:
      * micro-gameOfLife-webgui
        ```bash
        $ cd micro-gameOfLife-webgui/
        $ bash install_dev_env.sh
        ```
      * micro-gameOfLife-webapi
        ```bash
        $ cd micro-gameOfLife-webapi/
        $ mvn clean install
        ```
      * micro-gameOfLife-core
        ```bash
        $ cd micro-gameOfLife-core/
        $ mvn clean install
        ```
      * micro-gameOfLife-messagequeue
        ```bash
        $ cd micro-gameOfLife-messagequeue/
        $ mvn clean install
        ```
      * micro-gameOfLife-gridworker
        ```bash
        $ cd micro-gameOfLife-gridworker/
        $ mvn clean install
        ```
2. Build each container with the according `build.sh` script: 
      * micro-gameOfLife-webgui
        ```bash
        $ cd micro-gameOfLife-webgui/docker/
        $ bash build.sh <VERSION>
        ```
      * micro-gameOfLife-webapi
        ```bash
        $ cd micro-gameOfLife-webapi/docker/
        $ bash build.sh <VERSION>
        ```
      * micro-gameOfLife-gridworker
        ```bash
        $ cd micro-gameOfLife-gridworker/docker/
        $ bash build.sh <VERSION>
        ```
3. Run the service with docker-compose:
    ```bash
    $ docker-compose up
    ```
4. In your browser go to `http://localhost`