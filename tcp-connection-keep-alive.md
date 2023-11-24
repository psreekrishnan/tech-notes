### Keep listening on tcp port that handles multiple connections

cat script_name.sh

```bash
#!/bin/bash

while true
do
    nc -l -p <port_number> &
    wait $!
done
```

#### How to Run?
```
chmod +x script_name.sh
nohup sh script_name.sh &
```
#### Test you connection?
```
nc -zv <IP> <PORT>
Connection to <IP> <PORT> port [tcp/*] succeeded!
```

- This script continuously listens on the specified port (<port_number>) by looping the nc command. 
- The wait $! ensures that the loop waits for each instance of nc to finish before starting a new one. 
- This way, it handles multiple incoming connections.
