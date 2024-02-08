###############################################################
Integrated Toolbox Documentation
###############################################################



========
Development and Setup Instructions
========
Regarding the installation of the components, all component is providing instructions for the installation and usage as part of the documentation provided in the corresponding GitHub repositories. In addition, a central point of reference has been created for aggregating the information of all components and is provided in https://datacloud-project.github.io/toolbox/

DIS-PIPE
------------

DEF-PIPE
------------

SIM-PIPE
------------
Sandbox environment set up
~~~~~~~~~~
Tool Interface and Simulation Controller
~~~~~~~~~~

ADA-PIPE 
------------

R-MARKET
------------

DEP-PIPE
------------


========
DataCloud Testbed
========

All services are available for testing and are accessible through the toolbox landing page. For the final release all services will be provided with. DataCloud subdomain, as this will allow to overcome some Cross-origin resource sharing (CORS) issues and assist on the tighter integration of the platform. 

+------------------------+---------------------------------------------------+---------------------------------------------+
| Component              | IP, port or Current URL                           | Common domain used for demo                 |
+========================+===================================================+=============================================+
| Toolbox                | https://datacloud-toolbox.euprojects.net          | datacloud-toolbox.euprojects.net            |
+------------------------+---------------------------------------------------+---------------------------------------------+
| DIS-PIPE               | https://195.231.61.196:7778/                      | datacloud-dis.euprojects.net                |
+------------------------+---------------------------------------------------+---------------------------------------------+
| SIM-PIPE               | (locally installed) https://simpipe.sct.sintef.no | datacloud-sim.euprojects.net                |
+------------------------+---------------------------------------------------+---------------------------------------------+
| DEF-PIPE               | https://crowdserv.sys.kth.se                      | datacloud-def.euprojects.net                |
+------------------------+---------------------------------------------------+---------------------------------------------+
| ADA-PIPE               | http://194.182.187.139                            | datacloud-ada.euprojects.net                |
+------------------------+---------------------------------------------------+---------------------------------------------+
| DEP-PIPE               | 192.168.3.144:80                                  | datacloud-dep.euprojects.net                |
+------------------------+---------------------------------------------------+---------------------------------------------+
| R-MARKET               | http://20.71.159.181:10000                        | datacloud-market.euprojects.net             |
+------------------------+---------------------------------------------------+---------------------------------------------+
| Authentication service | https://datacloud-dep.euprojects.net/             | datacloud-auth.euprojects.net               |
+------------------------+---------------------------------------------------+---------------------------------------------+
| Monitoring             | 192.168.3.144:80                                  | https://datacloud-prometheus.euprojects.net |
+------------------------+---------------------------------------------------+---------------------------------------------+


.. In the User Dashboard landing page, the user can select among the available applications in her/his cluster.

.. By selecting the desired application, the user is redirected to the application’s page where she/he can find all the available information about the application. 
.. Here, the information is divided in three sections: 

.. A. Login and configure cluster.
.. B. And the Policies section where the user can view, add or delete policies.
.. C. The Components Deployment section, where the components of the application and the connection between them can be found.
.. D. The Incidents Representation section, which contains all the incidents that occur in any of the components.


.. Login
.. ------------

.. When the user visits the PUZZLE Dashboard’s URL, he will be asked to insert his credentials to enter the user interface. 
.. For this purpose, the Keycloak open source platform was utilized to handle the user management and access to the Dashboard

.. - Provide your login credentials and click the *Login* button.

.. .. image:: assets/keycloak_login.png

.. - Upon successful authentication the following screen will be presented. It provides an overview of the available use case deployments of the cybersecurity and monitoring agents. The deployments that each user can access will be specific to his role and organization.

.. .. image:: assets/welcome.jpg


.. ========
.. Infrastructure Setup
.. ========

.. - The first step for a user is to add her/his infrastructure. 
.. - To do so we press the Infrastructure link from the main menu on the left.

.. .. image:: assets/infra.jpg

.. - And then we press the **Add** button in the form that appears we fill up the fields.
.. - Name, with a desired name for our cluster and Configuration Content with the contents of the kube-config file from the kubernetes cluster…
.. - And  we press the **Submit** button.

.. .. image:: assets/new-cluster.jpg

.. - In the next page we can see, in the List of Clusters table, the cluster that we just added.
.. - By pressing the **View** button, we can view all the available information, such as the list of workers and their role in the cluster. 

.. .. image:: assets/view-nodes.jpg


.. You can also see the relevant video

.. .. raw:: html

..    <iframe src="https://drive.google.com/file/d/1ibjEnc-x-r9_nV2AdAO-LUwbGFq4cLYh/preview" width="640" height="480" allow="autoplay"></iframe>




.. ========
.. Policy Management
.. ========

.. Policy Templates  
.. ----------
.. - Policy templates (downloaded from Marketplace) can be configured and used in the dashboard.

.. .. image:: assets/templates.jpg

.. - Policy templates can be directly provided by the marketplace, or can be downloaded and manually transferred.

.. .. TODO changed image
.. .. .. image:: assets/upload-policy.jpg
.. .. image:: assets/marketplace_policy_add.png

.. .. TODO added
.. Policies template can be found in the Policy Template page

.. .. image:: assets/marketplace_policy_temp_page.png

.. .. TODO previous ver
.. .. Infrustructure Protection  
.. .. ----------
.. .. - Policies can be added for protection of nodes (in future releases of PUZZLE)

.. ========
.. Applications
.. ========

.. Application Setup  
.. ----------
.. ========
.. - To add an application we press the **Applications** link from the main menu on the left.

.. .. image:: assets/my-apps.jpg

.. - Then we press the  **Add** button. 

.. .. image:: assets/new-app.jpg

.. * We fill up the fields on the form that displays:

..   * **Name**, with a desired name for our application.
..   * **Cluster**, by selecting from a list of Clusters that we have created on the Infrastructures.
..   * And **Namespace**, by selecting from a list of Namespaces that are available in the Cluster that we select on the previous step.
 
.. - By clicking on the **Submit** button we transferred to a page where we can find the application that we just added in the List of Applications table.

.. .. image:: assets/my-apps.jpg

.. - There we can press the **View** button in order to see all the available information for that application, such as the list of the components and their kind.

.. .. image:: assets/appview.jpg


.. You can also see the relevant video:

.. .. raw:: html

..    <iframe src="https://drive.google.com/file/d/1XAbbmGXcOozHtRS9aer_v8WHnxqVJFm6/preview" width="640" height="480" allow="autoplay"></iframe>



.. Protect Application
.. ----------

.. To add policies to components we press the **Applications** link from the main menu on the left
.. - There we press the **View** button on the application that we choose.

.. .. image:: assets/appview.jpg


.. - In the desired component from the Components table we press the **Add Policy** button.
.. .. image:: assets/add-policy1.jpg


.. - From the list of the Available Policies we select the desired policy and we press the **Submit** button.

.. .. image:: assets/add-policy2.jpg


.. * After a while we can see the selected Policy on the Policies table.
  
..   * When a policy meets the criteria we can see the corresponding report on the Reports table.
..   * There we can see the exact time when the policy fired and by clicking on the event we can view the policy’s metadata.


.. You can also see the relevant video

.. .. raw:: html

..    <iframe src="https://drive.google.com/file/d/12ezmNN02sIRr9MHtw_LqQWEdlUm7z8iH/preview" width="640" height="480" allow="autoplay"></iframe>


.. .. TODO added
.. Risk Analysis
.. ----------
.. When a new application is added PUZZLE platform can automatically discover all the components and communicate that information with the PUZZLE Risk Assessment Engine which returns a report with all the known vulnerabilities about a component. 

.. By pressing **Vulnerabilities** button in the relevant component the user goes to the corresponding page.

.. .. image:: assets/marketplace_vulnerabilities.png

.. In the **Application** page there can be found the **Risk Analysis** button which leads to a page that contains the Risk Analysis for the application.

.. .. image:: assets/marketplace_risk_analysis.png

.. The Risk Analysis page contains information about the threats that each component (asset) faces combined with the vulnerabilities divided into categories from very high to very low risk

.. .. image:: assets/marketplace_risk_analysis3.png

.. .. TODO added
.. Reporting
.. ----------

.. The Reports are shown in a table that contains the timestamp when the report is generated and the name of the policy and are grouped by the components in which the policies are applied. Also, by pressing in the report event the users can find extra metadata about the specific report.

.. .. image:: assets/marketplace_reporting.png
   

.. ========
.. Threat Intelligence
.. ========

.. User can share content securely through CIDV

.. .. image:: assets/cidv.jpg



.. A video showing the usage of marketplace is available in the project's `repository <https://gitlab.com/puzzle-project/platform-usage-documentation>`_

.. .. TODO added
.. With the use of the CIDV, users can monitor available threat information displayed in a table, allowing for keyword searches. There's an option to open and examine a specific threat in its native data format, as well as an option to delete particular threats. The dashboard features complementary widgets that offer a comprehensive overview of the data stored in the blockchain network. A bar chart provides a snapshot of the vulnerabilities for each organization in the network, and a pie chart displays the number of vulnerabilities associated with each threat. These widgets collectively aid in drawing insights and facilitating deeper investigation into specific incidents by examining the raw data. Additionally, there's a feature to download the visual representations as images.

.. .. image:: assets/cidv_ui.png
