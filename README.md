Getting start to Elasticsearch

1.Download and uncompress package, then enter the base directory.

2.Configuration[config/elasticsearch.yml]
  important:
    a. get rid of '#' from items those named 
      node.name
      cluster.initial_master_nodes
      network.host
    b. modify network.host from default ip to 0.0.0.0 (otherwise localhost allowed only)

3.Dxcute [bin/elasticsearch -d] by normal user, cannot be root user 
  how to add normal user, like elastic
    add group: groupadd elastic
    add user useradd elastic -g elastic -p holly0
  how to switch to normal user, like elastic  
    su elastic
 
4.Stop elasticsearch service
  run the command as [kill -9 $elastic_process_id]
