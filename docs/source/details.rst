[--solutionname--] Details
============================

TML Solution DAG Parameters' Details
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

