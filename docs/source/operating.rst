[--solutionname--] Operating Details
====================================

.. important::
   These are the operating details for your TML solution.  

   It is important to note that this documentation will 

   dynamically update with the **Runtime Ports** for your solution.

   The ports below were valid for the last run of your solution.

.. tip::
   You must have your [--solutionname--] container running before connecting to the Visualization and Airflow URLs.

TSS Docker Run Command
-----------------------
This is the TML Solution Studio Docker Run command.  Note for MAC users change amd64 to arm64 in the container name. 

.. important::
   --tssdockerrun--

Your Solution Docker Container
--------------------------

.. important::
   --dockercontainer--

Your Solution Docker Run Command 
-----------------------
This is the Docker Run command for your solution container.  Note ports may change at runtime. The solution documentation will update automatically.

.. important::
   --dockerrun--

Your Solution Dashboard URL
-----------------------
This is the visualization URL for your TML dashboard. Note ports may change at runtime.  The solution documentation will update automatically.

.. important::
   --visualizationurl--

Solution Airflow URL
----------------
This is the Airflow URL for your solution container.  NOTE: While this is provided in the container - you should run/schedule solution containerss from the TSS.

.. important::
   --airflowurl--

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

