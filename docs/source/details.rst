[tssproject2-2b5c] Details
============================

Generated On: 2024-12-05 19:55:37 UTC

TML Solution DAG Parameters' Details: User Chosen Parametets
----------------------------

STEP 1: Get TML Core Params: `tml_system_step_1_getparams_dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-1-get-tml-core-params-tml-system-step-1-getparams-dag>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - solutionname
     - tssproject2-2b5c
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
     - MQTT
 
STEP 2: Create Kafka Topics: `tml_system_step_2_kafka_createtopic_dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-2-create-kafka-topics-tml-system-step-2-kafka-createtopic-dag>`_
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
     - cisco-network-mainstream
   * - preprocess_data_topic
     - cisco-network-preprocess
   * - ml_data_topic
     - ml-data
   * - prediction_data_topic
     - prediction-data

STEP 3: `Produce to Kafka Topics <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-3-produce-to-kafka-topics>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PRODUCETYPE
     - MQTT
   * - TOPIC
     - cisco-network-mainstream
   * - PORT
     - 41923
   * - IDENTIFIER
     - MQTT Subscription Topic: tml/cybersecurity
   * - HTTPADDR
     - https://
   * - FROMHOST
     - VanesaC,127.0.1.1
   * - TOHOST
     - 127.0.1.1
   * - CLIENTPORT
     - 8883
   * - TSS_CLIENTPORT
     - 8883
   * - TML_CLIENTPORT
     - 8883

STEP 4: Preprocesing Data: `tml-system-step-4-kafka-preprocess-dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-4-preprocesing-data-tml-system-step-4-kafka-preprocess-dag>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - cisco-network-mainstream
   * - preprocess_data_topic
     - cisco-network-preprocess
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
     - min,max,trend,anomprob,variance,avg
   * - pathtotmlattrs
     - --pathtotmlattrs--
   * - identifier
     - Detect potential cyber attacks and monitor network
   * - jsoncriteria
     - uid=hostName,filter:allrecords~subtopics=hostName,hostName,hostName~values=inboundpackets,outboundpackets,pingStatus~identifiers=inboundpackets,outboundpackets,pingStatus~datetime=lastUpdated~msgid=~latlong=

STEP 4b: Preprocesing Data: `tml-system-step-4b-kafka-preprocess-dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-4b-preprocesing-data-tml-system-step-4b-kafka-preprocess-dag>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - raw_data_topic
     - --raw_data_topic2--
   * - preprocess_data_topic
     - --preprocess_data_topic2--
   * - preprocessconditions
     - --preprocessconditions2--
   * - delay
     - --delay2--
   * - array
     - --array2--
   * - saveasarray
     - --saveasarray2--
   * - topicid
     - --topicid2--
   * - rawdataoutput
     - --rawdataoutput2--
   * - asynctimeout
     - --asynctimeout2--
   * - timedelay
     - --timedelay2--
   * - preprocesstypes
     - --preprocesstypes2--
   * - pathtotmlattrs
     - --pathtotmlattrs2--
   * - identifier
     - --identifier2--
   * - jsoncriteria
     - --jsoncriteria2--

STEP 5: Entity Based Machine Learning : `tml-system-step-5-kafka-machine-learning-dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-5-entity-based-machine-learning-tml-system-step-5-kafka-machine-learning-dag>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - cisco-network-preprocess
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
   * - processlogic
     - --processlogic--
   * - dependentvariable
     - --dependentvariable--
   * - independentvariables
     - --independentvariables--
   * - rollbackoffsets
     - --rollbackoffsets--
   * - topicid
     - -999
   * - consumefrom
     - cisco-network-preprocess
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

STEP 6: Entity Based Predictions: `tml-system-step-6-kafka-predictions-dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-6-entity-based-predictions-tml-system-step-6-kafka-predictions-dag>`_
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - preprocess_data_topic
     - cisco-network-preprocess
   * - ml_prediction_topic
     - --ml_prediction_topic--
   * - streamstojoin
     - --streamstojoin--
   * - inputdata
     - --inputdata--
   * - consumefrom
     - --consumefrom2--
   * - offset
     - -1
   * - delay
     - 70
   * - usedeploy
     - --usedeploy--
   * - networktimeout
     - --networktimeout--
   * - maxrows
     - --maxrows--
   * - topicid
     - -999
   * - pathtoalgos
     - --pathtoalgos--

STEP 7: Real-Time Visualization: `tml-system-step-7-kafka-visualization-dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-7-real-time-visualization-tml-system-step-7-kafka-visualization-dag>`_
^^^^^^^^^^^^^^^^^^^^^

.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - vipervizport
     - 9005
   * - topic
     - cisco-network-preprocess,cisco-network-privategpt
   * - dashboardhtml
     - tml-cisco-network-privategpt-monitor.html
   * - secure
     - 1
   * - offset
     - -1
   * - append
     - 0
   * - chip
     - amd64
   * - rollbackoffset
     - 400

STEP 8: `tml_system_step_8_deploy_solution_to_docker_dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-8-deploy-tml-solution-to-docker-tml-system-step-8-deploy-solution-to-docker-dag>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Docker Container
     - vanesalcb/tssproject2-2b5c-amd64 (https://hub.docker.com/r/vanesalcb/tssproject2-2b5c-amd64)
   * - Docker Run Command
     - docker run -d -p 37419:37419 -p 41445:41445 -p 46265:46265 -p 8883:8883 \
          --env TSS=0 \
          --env SOLUTIONNAME=tssproject2-2b5c \
          --env SOLUTIONDAG=solution_preprocessing_ai_mqtt_dag-tssproject2-2b5c \
          --env GITUSERNAME=vanesalcb06 \
          --env GITREPOURL=https://github.com/vanesalcb06/raspberrypi.git \
          --env SOLUTIONEXTERNALPORT=37419 \
          -v /var/run/docker.sock:/var/run/docker.sock:z  \
          --env CHIP=amd64 \
          --env SOLUTIONAIRFLOWPORT=41445  \
          --env SOLUTIONVIPERVIZPORT=46265 \
          --env DOCKERUSERNAME='vanesalcb' \
          --env CLIENTPORT=8883  \
          --env EXTERNALPORT=41923 \
          --env KAFKACLOUDUSERNAME='' \
          --env VIPERVIZPORT=9005 \
          --env MQTTUSERNAME='hivemq.webclient.1725974242180' \
          --env AIRFLOWPORT=9000  \
          --env GITPASSWORD='<Enter Github Password>' \
          --env KAFKACLOUDPASSWORD='<Enter API secret>' \
          --env MQTTPASSWORD='<Enter mqtt password>' \
          --env READTHEDOCS='<Enter Readthedocs token>' \
          vanesalcb/tssproject2-2b5c-amd64

STEP 9: `tml_system_step_9_privategpt_qdrant_dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-9-privategpt-and-qdrant-integration-tml-system-step-9-privategpt-qdrant-dag>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - PrivateGPT Container
     - maadsdocker/tml-privategpt-no-gpu-amd64
   * - PrivateGPT Run Command
     - docker run -d -p 8001:8001 --net=host --gpus all --env PORT=8001 --env GPU=1 --env COLLECTION=tml --env WEB_CONCURRENCY=1 --env CUDA_VISIBLE_DEVICES=0 maadsdocker/tml-privategpt-no-gpu-amd64
   * - Qdrant Container
     - qdrant/qdrant
   * - Qdrant Run Command
     - docker run -d -p 6333:6333 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant
   * - Consumefrom
     - cisco-network-preprocess
   * - pgpt_data_topic
     - cisco-network-privategpt
   * - offset
     - -1
   * - rollbackoffset
     - 400
   * - topicid
     - -999
   * - enabletls
     - 1
   * - partition
     - -1
   * - prompt
     - Do any of the values of the inbound or outbound packets look abnormal?
   * - context
     - These data are anomaly probabilities of suspicious data traffic. A high probability of over 0.80 is likely suspicious.
   * - jsonkeytogather
     - hyperprediction
   * - keyattribute
     - outboundpackets,inboundpackets
   * - keyprocesstype
     - anomprob
   * - vectordbcollectionname
     - tml
   * - concurrency
     - 1
   * - CUDA_VISIBLE_DEVICES
     - 0
   * - pgpthost
     - http://127.0.0.1
   * - pgptport
     - 8001
   * - hyperbatch
     - 0

STEP 10: `tml_system_step_10_documentation_dag <https://tml.readthedocs.io/en/latest/tmlbuilds.html#step-10-create-tml-solution-documentation-tml-system-step-10-documentation-dag>`_
^^^^^^^^^^^^^^^^^^^^^
.. list-table::

   * - **User Parameter**
     - **Chosen Value**
   * - Solution Documentation URL
     - https://tssproject2-2b5c.readthedocs.io
