# FAQ

## Vocareum Lab
---
### **Auto-disconnect**
---
**I have been working for a few hours on Vocareum, but I suddenly cannot access it. What happened?**

For Vocareum labs, there is **a time limit of 5 hours** for session. The session will be automatically disconnected once the 5 hours is up. 

You can check on the time left for your session from your work space, beside the “Start Lab” button (see image below). 

![Session Time](images/voc-session-time.png)

If your session is disconnected due to the time limit, you can re-access your lab by closing the lab and starting a new lab session.


### **Mongodb Connection Issue**
---
**Mongodb is disconnected. I am facing an error trying to reconnect Mongodb.**

Usually when this happens, it means that the previous Mongodb run was not logged off properly and the lock file was not removed.

For a quick fix, run the following commands on your terminal.

>`cd /home/labsuser/dbfiles`

>`rm -rfv WiredTiger.lock mongod.lock`

>`sudo mongod --dbpath /home/labsuser/dbfiles --repair`

Once you run the above commands, proceed to restart your lab by pressing “End Lab” on the top right corner of your workspace and press “Start Lab” to start it again.
![Start/End Lab](images/voc-start-end.png)