
---

## ✅ `networking-basics/ping-and-traceroute-examples.md` 


# 📡 Ping & Traceroute Examples

## 📶 What is `ping`?

Ping checks if a device is reachable over the network.
```markdown
### Example:
1. Go to CMD and type ping 8.8.8.8

📘 Output:

Reply = success

Request timed out = failed, if typed wrong.

Example of timed out:
"ping 8.8.8.
Ping request could not find host 8.8.8.. Please check the name and try again." This message will pop out.
```

🌐 What is tracert?


Tracert shows the path packets take to reach a host.


✅ What tracert does:


It shows the path your data takes to reach a destination (like 8.8.8.8 or google.com).

It helps identify where delays or failures happen in a network.

It sends small network packets (ICMP or UDP) and measures response time from each hop.

Sample Use to check: 
```markdown
After checking ping in CMD:
Ping Router:....
Ping DNS Server:.....

Enter as follows to check tracets of YOUTUBE:
tracert youtube.com

Will display as follows:
Tracing route to youtube.com (IPv6 address removed)
over a maximum of 30 hops:

  1     1 ms     1 ms     4 ms  
  2    17 ms    18 ms    18 ms  
  3    16 ms    16 ms    12 ms  
  4    18 ms    19 ms    22 ms  
  5    15 ms    22 ms    19 ms  
  6     *        *        *     Request timed out.
  7    19 ms    15 ms    16 ms  
  8    16 ms    21 ms    16 ms  
  9    15 ms    13 ms    15 ms  

Trace complete.
```

