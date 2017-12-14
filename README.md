# datastax-dse

curl -O -k --user DATASTAX-USERNAME:PASSWORD -L https://downloads.datastax.com/enterprise/dse-5.1.5-bin.tar.gz

tar -xvzf dse-5.1.5-bin.tar.gz

dse-5.1.5/bin/dse cassandra -R &

## Parameters to configure in "resources/cassandra/conf/cassandra.yaml"

row_cache_size_in_mb: 1000

-seeds: "<private ip1>,<private ip2>,<private ip3>"

listen_address: <private ip>

rpc_address: <private ip>

## Parameters to configure in "resources/dse/conf/dse.yaml"

max_memory_to_lock_fraction: 0.6 

max_memory_to_lock_mb: 10240  (We can keep this to 10 GB so that this will be taken up)




