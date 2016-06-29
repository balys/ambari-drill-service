# ambari-drill-service
Ambari service for Apache Drill

Ambari service to run and manage Apache Drill. For more information about Apache Drill visit <a href>https://drill.apache.org/</a>

  Requirements: <br>
    - RHEL/CENTOS 7.1 <br>
    - Ambari 2.X <br>
    - HDP 2.4 <br>
    - You need HDFS and Zookeeper up & running on your cluster
    
  Features: <br>
    - Allows to install Apache Drill on an Ambari-managed cluster <br>
    - Edit drill-overrides.conf and drill-env.sh via ambari <br>
    - Integration with zookeeper <br>



### Setup

Download the Drill Service:

```
VERSION=`hdp-select status hadoop-client | sed 's/hadoop-client - \([0-9]\.[0-9]\).*/\1/'`
git clone https://github.com/balys/ambari-drill-service.git /var/lib/ambari-server/resources/stacks/HDP/$VERSION/services/DRILL 
```

Restart ambari:

<code>
ambari-server restart
</code>

Now you can install Drill by clicking on "Add Service" button in Ambari
