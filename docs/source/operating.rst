[--solutionname--] Operating Details
====================================

.. important::
   These are the operating details for your TML solution.

.. tip::
   You must have your [--solutionname--] container running before connecting to the Visualization and Airflow URLs.

.. list-table::

   * - **Type**
     - **Details**
     - **Explanation**
   * - Docker Container
     - --dockercontainer--
     - This is the name of your solution container
   * - Docker Run Command
     - --dockerrun--
     - This is the Docker Run command for your 

       solution container.  Note ports may change at runtime. 

       The solution documentation will update automatically.
   * - Visualization URL
     - --visualizationurl--
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
     - --tmlbinaries--
     - These are the ports the TML binaries 

       are listening on.
   * - TMUX Windows
     - --tmuxwindows--
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

       
