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
     - This is the Docker Run command for your solution container
   * - Visualization URL
     - --visualizationurl--
     - This is the visualization URL for your TML dashboard
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
     - This is the name of the solution DAG you chose to trigger 
   * - TML Binaries Listening Ports
     - --tmlbinaries--
     - These are the ports the TML binaries are listening on.

       when your container starts.
