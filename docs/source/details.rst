[myawesometmlsolution] Details
============================

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: tml_system_step_1_getparams_dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - myawesometmlsolution
   * - solutiontitle
     - My Solution Title
   * - solutiondescription
     - This is an awesome real-time solution built by TSS
   * - brokerhost
     - 127.0.0.1
   * - brokerport
     - 9092
   * - cloudusername
     - None
   * - ingestdatamethod
     - localfile
 
STEP 2: Create Kafka Topics: tml_system_step_2_kafka_createtopic_dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - companyname
     - Otics
   * - myname
     - Sebastian
   * - myemail
     - Sebastian.Maurice
   * - mylocation
     - Toronto
   * - replication
     - 1
   * - numpartitions
     - 1
   * - enabletls
     - 1
   * - microserviceid
     - 
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess-data,iot-preprocess2-data
   * - ml_data_topic
     - ml-data
   * - prediction_data_topic
     - prediction-data

STEP 3: Produce to Kafka Topics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PRODUCETYPE
     - LOCALFILE
   * - TOPIC
     - iot-raw-data
   * - PORT
     - --PORT--
   * - IDENTIFIER
     - TML solution

STEP 4: Preprocesing Data: tml-system-step-4-kafka-preprocess-dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - iot-raw-data
   * - preprocess_data_topic
     - iot-preprocess-data,iot-preprocess2-data
   * - preprocessconditions
     - 
   * - delay
     - 70
   * - array
     - 0
   * - saveasarray
     - 1
   * - topicid
     - -999
   * - rawdataoutput
     - 1
   * - asynctimeout
     - 120
   * - timedelay
     - 0
   * - preprocesstypes
     - anomprob,trend,avg,entropy,kurtosis
   * - pathtotmlattrs
     - --pathtotmlattrs--
   * - identifier
     - TML solution
   * - jsoncriteria
     - uid=metadata.dsn,filter:allrecords~subtopics=metadata.property_name~values=datapoint.value~identifiers=metadata.display_name~datetime=datapoint.updated_at~msgid=datapoint.id~latlong=lat:long

STEP 5: Entity Based Machine Learning : tml-system-step-5-kafka-machine-learning-dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - iot-preprocess-data,iot-preprocess2-data
   * - ml_data_topic
     - ml-data
   * - modelruns
     - --modelruns--
   * - offset
     - -1
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
     - -999
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
     - iot-preprocess-data,iot-preprocess2-data
   * - ml_prediction_topic
     - --ml_prediction_topic--
   * - streamstojoin
     - --streamstojoin--
   * - inputdata
     - --inputdata--
   * - consumefrom
     - --consumefrom--
   * - offset
     - -1
   * - delay
     - 70
   * - usedeploy
     - --usedeploy--
   * - networktimeout
     - --networktimeout--
   * - preprocess_data_topic
     - iot-preprocess-data,iot-preprocess2-data
   * - maxrows
     - --maxrows--
   * - topicid
     - -999
   * - pathtoalgos
     - --pathtoalgos--

STEP 7: Real-Time Visualization: tml-system-step-7-kafka-visualization-dag
^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - vipervizport
     - 54881
   * - topic
     - iot-preprocess
   * - secure
     - 1
   * - offset
     - -1
   * - append
     - 0
   * - chip
     - AMD64
   * - rollbackoffset
     - 500

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
