1. log out of the username that issued the interrupted work to that gpu

2. as root, find all running processes associated with the username that issued the interrupted work on that gpu:

ps -ef|grep username

3. as root, kill all of those

4. as root, retry the nvidia-smi gpu reset

5. sudo fuser -v /dev/nvidia*
