#!/bin/bash

# Simple Port Scanner using netcat (nc)

# Usage: ./port_scanner.sh <host> <start_port> <end_port>

HOST=$1
START_PORT=$2
END_PORT=$3

if [ -z "$HOST" ] || [ -z "$START_PORT" ] || [ -z "$END_PORT" ]; then
  echo "Usage: $0 <host> <start_port> <end_port>"
  exit 1
fi

echo "Scanning host: $HOST from port $START_PORT to $END_PORT..."

for (( port=$START_PORT; port<=$END_PORT; port++ ))
do
  nc -zv -w 1 $HOST $port &>/dev/null && echo "Port $port is OPEN" || echo "Port $port is CLOSED"
done

echo "Scan complete."

# Instructions to push to GitHub:
# 1. git init
# 2. git add port_scanner.sh
# 3. git commit -m "Add port scanning script"
# 4. git branch -M main
# 5. git remote add origin <your-github-repo-url>
# 6. git push -u origin main
