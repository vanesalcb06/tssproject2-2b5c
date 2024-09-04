[--solutionname--] Operating Details
====================================

.. important::
   These are the operating details for your TML solution.  

   It is important to note that this documentation will 

   dynamically update with the **Runtime Ports** for your solution.

   The ports below were valid for the last run of your solution.

.. tip::
   You must have your [--solutionname--] container running before connecting to the Visualization and Airflow URLs.

.. list-table::

   * - **Type**
     - **Details**
     - **Explanation**
   * - TML Solution Studio Docker Run Command
     - :ref:`TSS Docker Run Command`
     - This is the TML Solution Studio Docker Run command.  

       Note for MAC users change amd64 to arm64 in 

       the container name. 
   * - Your Solution Docker Container
     - --dockercontainer--
     - This is the name of your solution container
   * - Your Solution Docker Run Command
     - :ref:`Your Solution Docker Run Command`
     - This is the Docker Run command for your 

       solution container.  Note ports may change at runtime. 

       The solution documentation will update automatically.
   * - Visualization URL
     - :ref:`Your Solution Dashboard URL`
     - This is the visualization URL for your 

       TML dashboard. Note ports may change at runtime. 

       The solution documentation will update automatically.
   * - Solution Airflow URL
     - --airflowurl--
     - This is the Airflow URL for your solution container.  

       NOTE: While this is provided in the container - you 

       should run/schedule solution containerss from the TSS
   * - [--solutionname--] Github Repo
     - --gitrepo--
     - This is the Github repo for all your solution code
   * - Readthedocs URL
     - --readthedocs--
     - This is this url.
   * - Solution Trigger DAG
     - --triggername--
     - This is the name of the solution DAG you 

       chose to trigger 
   * - TML Binaries Listening Ports
     - :ref:`Your Solution TML Binaries`
     - These are the ports the TML binaries 

       are listening on.
   * - TMUX Windows
     - :ref:`Your Solution TMUX Windows`
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

TSS Docker Run Command
-----------------------
This is the TML Solution Studio Docker Run command.  Note for MAC users change amd64 to arm64 in the container name. 

.. important::
   --tssdockerrun--

Your Solution Docker Run Command 
-----------------------

.. important::
   --dockerrun--

Your Solution Dashboard URL
-----------------------

.. important::
   --visualizationurl--

Your Solution TML Binaries 
-----------------------

.. important::
   --tmlbinaries--

Your Solution TMUX Windows 
-----------------------

.. important::
   --tmuxwindows--
