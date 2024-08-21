[--solutionname--] Details
============================

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: tml_system_step_1_getparams_dag
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - --sname--
   * - solutiontitle
     - --stitle--
   * - solutiondescription
     - --sdesc--
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

STEP 4: Preprocesing Data: tml-system-step-4-kafka-preprocess-dag.py
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

STEP 5: Entity Based Machine Learning : tml-system-step-5-kafka-machine-learning-dag.py
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

