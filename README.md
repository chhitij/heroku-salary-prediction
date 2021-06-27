# Salary Prediction Deployment over Heroku and AWS

---

### Create virtual envoirnment

* tp create an env --conda create -n <env_name> <python_ver>

* eg conda create -n deployment python==3.7

* conda activate <env_name>

* install flask == > pip install flask

* conda config --set ssl_verify no

* install sckitlearn -pip install sckit-learn

* conda env list // getting all the envoirnment

* pip freeze > <fileName>requirment.txt</FileName>

* pip install -r requirment.txt // for saving all the package in other system
---
  ### Flask
  #### Note
      * Falsk is best for micro app for personal uses
      * Django is for production app industrial purpuse
  ---
   #### Deployment over heuruku

    * Add Procfile - > web: gunicorn fileName(main):appName(from file)
    * web: guincorn == > networking stuff
    * app:main --> pthon main.py Pass (platform depended)
    * install gunicorn in your env
    * create a requirement .txt file
    * create a file called Procfile
    * upload all files over github
   ---
  #### Deployment with AWS
      ##### For Window user
    * Download putty.org
    * Download winscp
    * amazon console - > launch a virtual machine
    * search ubuntu -> select free tire
    * select virtual env and save key and launch
    * Select puttygen
    * load .pem file
    * save pvt file
    * winScp and conncet amazon instance get u_name and host name 
      * for getting host name click on ssh client,
        and click on authticate and slect pvt key what we saved for putty and connect 
      * install python3
      * for open file vi <fileName>
      * add port(host=0,0,0,0 , port =8080 )
      ecs :wq
      * create sceruty group and add new group in inbound group
      * inbound rule -> add all traffic
      * click network interface -> sceurity groups -> change sceurity groups
      go to instance and copy ssc and paste in usl and add : 8080

