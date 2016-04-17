# exercise1_memoryCheck
#This is the script for Exit code
#!/bin/bash
TOTAL_MEMUSED=$( free | grep Mem: | awk '{ printf "%.0f", $3/$2 * 100 }' )

feed="/root/scripts/smp4.sh"

$feed $1 $2 $3 $4 $5 $6

case $? in

2)
  echo "Memory is at $TOTAL_MEMUSED % . CRITICAL Threshold"
  ;;
1)
  echo "Memory is at $TOTAL_MEMUSED % . WARNING Threshold"
  ;;
0)
  echo "Memory is at $TOTAL_MEMUSED % . NORMAL Threshold"
  ;;
3)
   echo ""
;;
esac
