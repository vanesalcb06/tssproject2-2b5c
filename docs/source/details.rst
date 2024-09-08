[--solutionname--] Details
============================

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: `tml_system_step_1_getparams_dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-1-get-tml-core-params-tml-system-step-1-getparams-dag>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - --solutionname--
   * - solutiontitle
     - --solutiontitle--
   * - solutiondescription
     - --solutiondescription--
   * - brokerhost
     - --brokerhost--
   * - brokerport
     - --brokerport--
   * - cloudusername
     - --cloudusername--
   * - ingestdatamethod
     - --ingestdatamethod--
 
STEP 2: Create Kafka Topics: tml_system_step_2_kafka_createtopic_dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - companyname
     - --companyname--
   * - myname
     - --myname--
   * - myemail
     - --myemail--
   * - mylocation
     - --mylocation--
   * - replication
     - --replication--
   * - numpartitions
     - --numpartitions--
   * - enabletls
     - --enabletls--
   * - microserviceid
     - --microserviceid--
   * - raw_data_topic
     - --raw_data_topic--
   * - preprocess_data_topic
     - --preprocess_data_topic--
   * - ml_data_topic
     - --ml_data_topic--
   * - prediction_data_topic
     - --prediction_data_topic--

STEP 3: Produce to Kafka Topics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PRODUCETYPE
     - --PRODUCETYPE--
   * - TOPIC
     - --TOPIC--
   * - PORT
     - --PORT--
   * - IDENTIFIER
     - --IDENTIFIER--
   * - HTTPADDR
     - --HTTPADDR--
   * - FROMHOST
     - --FROMHOST--
   * - TOHOST
     - --TOHOST--
   * - CLIENTPORT
     - --CLIENTPORT--
   * - TSS_CLIENTPORT
     - --TSSCLIENTPORT--
   * - TML_CLIENTPORT
     - --TMLCLIENTPORT--

STEP 4: Preprocesing Data: tml-system-step-4-kafka-preprocess-dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic--
   * - preprocess_data_topic
     - --preprocess_data_topic--
   * - preprocessconditions
     - --preprocessconditions--
   * - delay
     - --delay--
   * - array
     - --array--
   * - saveasarray
     - --saveasarray--
   * - topicid
     - --topicid--
   * - rawdataoutput
     - --rawdataoutput--
   * - asynctimeout
     - --asynctimeout--
   * - timedelay
     - --timedelay--
   * - preprocesstypes
     - --preprocesstypes--
   * - pathtotmlattrs
     - --pathtotmlattrs--
   * - identifier
     - --identifier--
   * - jsoncriteria
     - --jsoncriteria--

STEP 5: Entity Based Machine Learning : tml-system-step-5-kafka-machine-learning-dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - --preprocess_data_topic--
   * - ml_data_topic
     - --ml_data_topic--
   * - modelruns
     - --modelruns--
   * - offset
     - --offset--
   * - islogistic
     - --islogistic--
   * - networktimeout
     - --networktimeout--
   * - modelsearchtuner
     - --modelsearchtuner--
   * - dependentvariable
     - --dependentvariable--
   * - independentvariables
     - --independentvariables--
   * - rollbackoffsets
     - --rollbackoffsets--
   * - topicid
     - --topicid--
   * - consumefrom
     - --consumefrom--
   * - fullpathtotrainingdata
     - --fullpathtotrainingdata--
   * - transformtype
     - --transformtype--
   * - sendcoefto
     - --sendcoefto--
   * - coeftoprocess
     - --coeftoprocess--
   * - coefsubtopicnames
     - --coefsubtopicnames--

STEP 6: Entity Based Predictions: tml-system-step-6-kafka-predictions-dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - --preprocess_data_topic--
   * - ml_prediction_topic
     - --ml_prediction_topic--
   * - streamstojoin
     - --streamstojoin--
   * - inputdata
     - --inputdata--
   * - consumefrom
     - --consumefrom--
   * - offset
     - --offset--
   * - delay
     - --delay--
   * - usedeploy
     - --usedeploy--
   * - networktimeout
     - --networktimeout--
   * - maxrows
     - --maxrows--
   * - topicid
     - --topicid--
   * - pathtoalgos
     - --pathtoalgos--

STEP 7: Real-Time Visualization: tml-system-step-7-kafka-visualization-dag
^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - vipervizport
     - --vipervizport--
   * - topic
     - --topic--
   * - secure
     - --secure--
   * - offset
     - --offset--
   * - append
     - --append--
   * - chip
     - --chip--
   * - rollbackoffset
     - --rollbackoffset--

STEP 8: tml_system_step_8_deploy_solution_to_docker_dag
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Docker Container
     - --dockercontainer--
   * - Docker Run Command
     - --dockerrun--

STEP 9: tml_system_step_9_privategpt_qdrant_dag
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PrivateGPT Container
     - --privategptcontainer--
   * - PrivateGPT Run Command
     - --privategptrun--
   * - Qdrant Container
     - --qdrantcontainer--
   * - Qdrant Run Command
     - --qdrantrun--

STEP 10: tml_system_step_10_documentation_dag
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Solution Documentation URL
     - --readthedocs--
