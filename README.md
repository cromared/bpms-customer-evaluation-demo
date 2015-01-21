JBoss BPM Suite Customer Evaluation Demo
========================================
The customer evaluation project demonstrates the BPM Suite process integration with rules.
It is a straight through process (STP).

There are three options available to you for using this demo; local, Openshift and Docker.


Option 1 - Install on your machine
----------------------------------
1. [Download and unzip.](https://github.com/jbossdemocentral/bpms-customer-evaluation-demo/archive/master.zip)

2. Add products to installs directory.

3. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges. 

4. Start JBoss BPMS Server by running 'standalone.sh' or 'standalone.bat' in the <path-to-project>/target/jboss-eap-6.1/bin directory.

5. Login to http://localhost:8080/business-central  (u:erics / p:bpmsuite1!).

6. Customer Evaluation demo pre-installed as project.

7. Process and Task dashboard pre-filled with mock data optional now. For Windows installer, to add just uncomment install scripts
	 (see inline script comments).

8. Read the documentation found in the docs directory & enjoy JBoss BPM Suite!


Option 2 - Install with one click in xPaaS (bpmPaaS)
----------------------------------------------------
After clicking button, ensure `Gear` size is set to `medium`:

[![Click to install OpenShift](http://launch-shifter.rhcloud.com/launch/light/Install bpmPaaS.svg)](https://openshift.redhat.com/app/console/application_type/custom?&cartridges[]=https://raw.githubusercontent.com/jbossdemocentral/cartridge-bpmPaaS-customer-evaluation-demo/master/metadata/manifest.yml&name=customerevaluation&gear_profile=medium&initial_git_url=)

Once installed you can use the JBoss BPM Suite login: 

   * u:erics   p: bpmsuite  (admin)

   * u: alan   p: bpmsuite  (analyst)

   * u: daniel p: bpmsuite (developer)

   * u: ursla  p: bpmsuite (user)

   * u: mary   p: bpmsuite (manager)


Option2 - Generate docker install
---------------------------------
The following steps can be used to configure and run the demo in a docker container

1. [Download and unzip.](https://github.com/jbossdemocentral/bpms-customer-evaluation-demo/archive/master.zip)

2. Add product installer to installs directory.

3. Copy contents of support/docker directory to the project root.

4. Build demo image.

	```
	docker build -t jbossdemocentral/bpms-customer-evaluation-demo .
	```
5. Start demo container

	```
	docker run --it -p 8080:8080 -p 9990:9990 jbossdemocentral/bpms-customer-evaluation-demo
	```
6. Login to http://<DOCKER_HOST>:8080/business-central (u:erics / p:bpmsuite1!)

7. Customer Evaluation demo pre-installed as project.

8. Read the documentation found in the docs directory & enjoy JBoss BPM Suite!

Additional information can be found in the jbossdemocentral docker [developer repository](https://github.com/jbossdemocentral/docker-developer)


Notes
-----
This project is pre-loaded into the JBoss BPM Suite, after starting it you can login,
examine the rule, process, and data model from within the various product components.
You can then build and deploy the project, thereby generating the kjar maven artifact 
that the developer team needs to begin working on any application using this projects
knowledge artifacts.

Once you setup the project in JBoss Developer Studio (see the docs), you can use maven 
to pull in the kjar dependency, then examine the unit tests to discover how an application
can interact with a knowledge project (rules, processes, and model).


Supporting Articles
-------------------
[3 shockingly easy ways into JBoss rules, events, planning & BPM](http://www.schabell.org/2015/01/3-shockingly-easy-ways-into-jboss-brms-bpmsuite.html)

[Jump Start Your Rules, Events, Planning and BPM Today](http://www.schabell.org/2014/12/jump-start-rules-events-planning-bpm-today.html)

[5 Handy Tips From JBoss BPM Suite For Release 6.0.3](http://www.schabell.org/2014/10/5-handy-tips-from-jboss-bpmsuite-release-603.html)

[Launching Into the Clouds With 2 New OpenShift Primer bpmPaaS Quickstarts](http://www.schabell.org/2014/10/launching-into-clouds-with-2-new-openshift-primer-bpmpaas-quickstarts.html)

[Red Hat JBoss BPM Suite - all product demos updated for version 6.0.2.GA release](http://www.schabell.org/2014/07/redhat-jboss-bpmsuite-product-demos-6.0.2-updated.html)


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.6 - JBoss BPM Suite 6.0.3 installer with optional docker installation.

- v1.5 - moved to JBoss Demo Central, updated windows init.bat support and one click install button.

- v1.4 - JBoss BPM Suite 6.0.3 installer with cutomer evalutation demo installed.

- v1.3 - JBoss BPM Suite 6.0.2 installer used, with cutomer evalutation demo installed.

- v1.2 - JBoss BPM Suite 6.0.2, JBoss EAP 6.1.1, and migrated JBDS project from BRMS 5.3.

- v1.1 - JBoss BPM Suite 6.0.1, JBoss EAP 6.1.1, and migrated JBDS project from BRMS 5.3.

- v1.0 - JBoss BPM Suite 6.0.0, JBoss EAP 6.1.1, and migrated JBDS project from BRMS 5.3.

- v0.7 - JBoss BPM Suite 6.0.0.CR2, JBoss EAP 6.1.1, and migrated JBDS project from BRMS 5.3.

- v0.6 - JBoss BPM Suite 6.0.0.CR1, JBoss EAP 6.1.1, and migrated JBDS project from BRMS 5.3.

- v0.5 - JBoss BPM Suite 6.0.0.Beta, JBoss EAP 6.1.1, mock data populated in Process and Task dashboard, and migrated JBDS project from BRMS 5.3.

- v0.4 - JBoss BPM Suite 6.0.0.Beta, JBoss EAP 6.1.1, migrated JBDS project from BRMS 5.3.

- v0.3 - JBoss BPM Suite 6.0.0.ER5, JBoss EAP 6.1, migrated JBDS project from BRMS 5.3, and full documentation.

- v0.2 - JBoss BPM Suite 6.0.0.ER5, JBoss EAP 6.1, and migrated JBDS project from BRMS 5.3.

- v0.1 - JBoss BPM Suite 6.0.0.Beta1, JBoss EAP 6.1, and migrated JBDS project from BRMS 5.3.


![Process](https://github.com/jbossdemocentral/bpms-customer-evaluation-demo/blob/master/docs/demo-images/process.png?raw=true)

![Process & Task Dashboard](https://github.com/jbossdemocentral/bpms-customer-evaluation-demo/blob/master/docs/demo-images/mock-bpm-data.png?raw=true)

