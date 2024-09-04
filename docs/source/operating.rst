[--solutionname--] Operating Details
====================================

.. important::
   These are the operating details for your TML solution.  

   It is important to note that this documentation will 

   dynamically update with the **Runtime Ports** for your solution.

   The ports below were valid for the last run of your solution, and will 

   **not be valid if your [--solutionname--] container is NOT running**.

.. tip::
   You must have your [--solutionname--] container running before connecting to the Visualization and Airflow URLs.

TSS Docker Run Command
-----------------------
This is the TML Solution Studio Docker Run command.  Note for MAC users change amd64 to arm64 in the container name. 

.. important::
   --tssdockerrun--

TSS Docker Run Command: Parameter Explanation
^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **Parameter**
     - **Explanation**
   * - docker
     - This calls the docker engine
   * - -d
     - This runs your container in **detached** mode
   * - \-\-net=host
     - This give your container access to your host operating system
   * - -v
     - This stands for **volume mapping**.  It maps a local folder

       in your host machine to the folder in the container.  The value **z**

        means the container has **shared access** to your local folder.

        For example, -v /mylocal/folder:/dagslocalbackup:z, means map 

        /mylocal/folder (on my host machine) to **/dagslocalbackup**

        in the contaner.   This allows files generated in the container 

        to be automatically written to your local folder.

   * - \-\-env GITREPOURL
     - This is your Github repo, that you cloned from **https://github.com/smaurice101/raspberrypi**
   * -  \-\-env CHIP=AMD64
     - This is the chip if your are running the TSS on windows/linux.

       If you are running MAC, use **CHIP=ARM64**
   * - \-\-env TSS=1
     - This is the TSS value and MUST be 1.
   * - \-\-env AIRFLOWPORT
     - This is the airflow port for TSS.  Connect to TSS from your browser:

       http://localhost:--airflowport--
   * - \-\-env SOLUTIONAIRFLOWPORT
     - This is the airflow port for TML solution.  Connect to TSS from your browser:

       http://localhost:--solutionairflowport--

       Note: If SOLUTIONAIRFLOWPORT=-1, then TSS gets a free port randomly.
   * - \-\-env SOLUTIONNAME=TSS
     - This is the solution name.
   * - \-\-env VIPERVIZPORT
     - This is the port the Viperviz binary will listen on for connections.

       Note: If VIPERVIZPORT=-1, a random free port is selected by TSS.
   * - \-\-env EXTERNALPORT=--externalport--
     - This is the external port that will be assigned to your TML solution for external access.

       You will need this port in the `REST <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3b-i-rest-api-client>`_, and `gRPC 
       <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3c-i-grpc-api-client>`_ clients.

       Note: if EXTERNALPORT=-1, TSS will choose a free port randomly.

       This external port is used by `Viper binary <https://tml.readthedocs.io/en/latest/usage.html>`_: Viper will be listening on this port 

       for a connection as shown here: :ref:`Your Solution TML Binaries`

       In the TMUX window **Viper-produce**: :ref:`Your Solution TMUX Windows`
   * - \-\-env READTHEDOCS
     - This is the readthedocs API token you created.

       Refer to: `Set up readthedocs <https://tml.readthedocs.io/en/latest/readthedocs.html>`_
   * - \-\-env  GITUSERNAME
     - This is your Githib username.
   * - \-\-env GITPASSWORD
     - This is the Github Personal Access Token you created.

       Refer to: `Creating Github Token: <https://tml.readthedocs.io/en/latest/docker.html#generating-personal-access-tokens-in-github>`_
   * - \-\-env DOCKERUSERNAME
     - This is your `Docker Hub <https://hub.docker.com/>`_ username.
   * - \-\-env DOCKERPASSWORD
     - This is your Docker Hub password.
   * - maadsdocker/tml-solution-studio-with-airflow-amd64
     - This is the TSS container name for AMD64

       If using MAC/Unix use: maadsdocker/tml-solution-studio-with-airflow-arm64

Your Solution Docker Container
--------------------------

.. important::
   --dockercontainer--

Your Solution Docker Run Command: Parameter Explanation
^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **Parameter**
     - **Explanation**
   * - docker
     - This calls the docker engine
   * - -d
     - This runs your container in **detached** mode
   * - \-\-net=host
     - This give your container access to your host operating system
   * - \-\-env TSS=0
     - Internal TSS variable. MUST be 0.
   * - \-\-env SOLUTIONNAME
     - This is the name of your TML solution.
   * - \-\-env SOLUTIONDAG
     - This is the name of the DAG that comprises your solution.

       This DAG is triggered automatically when you run this container.
   * - \-\-env  VIPERVIZPORT=--vipervizport--
     - This is the port Viperviz is listening.  

       You point your browser to this port. See :ref:`Your Solution Dashboard URL`
   * - \-\-env  SOLUTIONAIRFLOWPORT
     - This is the port for Airflow in TML solution container.

       Note: This is provided mainly for debugging and testing purposes only.
   * - \-\-env  GITUSERNAME
     - This is your Github username.
   * - \-\-env GITPASSWORD
     - This is the Github Personal Access Token you created.

       Refer to: `Creating Github Token: <https://tml.readthedocs.io/en/latest/docker.html#generating-personal-access-tokens-in-github>`_
   * - \-\-env GITREPOURL
     - This is your Github repo, that you cloned from **https://github.com/smaurice101/raspberrypi**
   * - \-\-env READTHEDOCS
     - This is the readthedocs API token you created.

       Refer to: `Set up readthedocs <https://tml.readthedocs.io/en/latest/readthedocs.html>`_
   * - \-\-env CHIP=--chip--
     - This is the chip family of your OS.
   * - \-\-env EXTERNALPORT=--externalport--
     - This is the external port that you can use when making an external connection to your TML solution

       for external data ingestion.  You will need this port in the `REST <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3b-i-rest-api-client>`_, and `gRPC <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3c-i-grpc-api-client>`_ clients.

       Note: if EXTERNALPORT=-1, TSS will choose a free port randomly.

       This external port is used by `Viper binary <https://tml.readthedocs.io/en/latest/usage.html>`_: Viper will be listening on this port 

       for a connection as shown here: :ref:`Your Solution TML Binaries`

       In the TMUX window **Viper-produce**: :ref:`Your Solution TMUX Windows` 
   * - --containername--
     - Your solution container name. 

Your Solution Docker Run Command 
-----------------------
This is the Docker Run command for your solution container.  Note ports may change at runtime. The solution documentation will update automatically.

.. important::
   --dockerrun--

Your Solution External Port
-----------------------
This is the Docker Run command for your solution container.  Note ports may change at runtime. The solution documentation will update automatically.

.. important::
   --externalport--

Your Solution Dashboard URL
-----------------------
This is the visualization URL for your TML dashboard. Note ports may change at runtime.  The solution documentation will update automatically.

.. important::
   --visualizationurl--

Your Solution Dashboard URL: Parameter Explanation
^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **Parameter**
     - **Explanation**
   * - http://localhost:<--vipervizport-->/<html file>
     - This is the URL pointing to an html file running inside your solution container.

       Refer to: `TML Real-time dashboards <https://tml.readthedocs.io/en/latest/dashboards.html>`_
   * - VIPERVIZPORT
     - This is the port Viperviz is listening on.
   * - topic
     - This is the topic that the TML binary `Viperviz <https://tml.readthedocs.io/en/latest/usage.html>`_ 

       is reading (consuming) in Apache Kafka and sending it to your broweser over websockets.  
   * - offset
     - This value tells the Viperviz binary to read the latest real-time data. 

       **offset=-1**, means to go to the end of the data stream and get the latest record.
   * - groupid
     - This can be empty. 
   * - rollbackoffset
     - This is the number of offsets to **rollback** the data stream from the **offset** value.

       Note: If you increase this number, Viperviz will send more data to your browser.  

       But be carefull, too much data may crash your browser or computer.
   * - topictype
     - Leave as is.
   * - append
     - This tells your html file whether to append or not the data streaming to your browser.

       If append=0, the html will not apend, if append=1, then data will accumulate in your browser.
   * - secure
     - This tells Viperviz whether to encrypt your data to the browser.  

       If secure=1, data are encrypted, secure=0 no encryption.

[--solutionname--] Github Repo
---------------
This is the Github repo for all your solution code

.. important::
   --gitrepo--

Readthedocs URL
---------------
This is this URL.

.. important::
   --readthedocs--

Solution Trigger DAG
----------------
This is the name of the solution DAG you chose to trigger.

.. important::
   --triggername--

Your Solution TML Binaries 
-----------------------
These are the ports the TML binaries are listening on.

.. important::
   --tmlbinaries--

Your Solution TMUX Windows 
-----------------------

.. important::
   --tmuxwindows--

- Your solution is running in these  

       TMUX windows:
   
        - To view windows, type:

          **tmux ls**

        - To go inside window, type:

          **tmux a -t <window name>**

        - To exit window, type:

          **CTLR+b, d**

        - To scroll window, type:

          **CTLR+b, [**

        - To un-scroll window, type:

          **CTLR+[**

