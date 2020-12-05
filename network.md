
# TCP Slow Start / 14kb rule

https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work 

The first response packet will be 14Kb. This is part of TCP slow start, an algorithm which balances the speed of a network connection. Slow start gradually increases the amount of data transmitted until the network's maximum bandwidth can be determined.
In TCP slow start, after receipt of the initial packet, the server doubles the size of the next packet to around 28Kb. Subsequent packets increase in size until a predetermined threshold is reached, or congestion is experienced.
