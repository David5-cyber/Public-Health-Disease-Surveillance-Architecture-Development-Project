# Public-Health-Disease-Surveillance-Architecture-Development-Project
This project simulates a regional healthcare IT architecture using virtual machines, OpenEMR, Synthea, and HAPI-FHIR to support electronic health records, disease outbreak modeling, and real-time public health surveillance. It includes VM setup, EHR deployment, synthetic data generation, FHIR-based data exchange, and dashboard visualization for COVID-19 trends across multiple hospitals
# Architecture Development Part 1: Virtual Machine Configuration/Testing
This project was focused on building a healthcare network using five virtual machines (VMs)—four representing hospitals namely;Aspirus Hospital,Portage Health,Baraga County Memorial Hospital,and Marquette General Hospital and one for the Upper Peninsula Health Information Exchange (UPHIE). The hospital VMs will run an OS compatible with OpenEMR, while the UPHIE VM will support HAPI-FHIR. All VMs  shared a common IP scheme to enable seamless connectivity and data exchange. The goal is to create a safe, controlled environment to explore health IT architecture, EMR systems, and interoperability standards like FHIR, bridging classroom concepts with real-world healthcare technology applications.
steps involved in setting up the virtual machine environment:

1.Establishment of a VPN connection

2.Accessed the institution's cluster

3.Navigated the virtual machines

4.Deployed and configured virtual marchines

5.Configured all five(5) virtual machines to operate within the same IP address range and subnet

6.Assigned each virtual machine to a hospital

The table below shows compatibility followed by a screenshot of the virtual machines created
![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/9d0a46f4be536f8a69a75d240737b6190afadacc/Screenshot%202025-04-17%20205010.png)
![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/24a731c95f569b5c732627f0cce948de524a6c71/Screenshot%202025-04-17%20212956.png)

# Architecture Development Part 2:Installation, Configuration and Security of OpenEMR
 In this project, i installed and configured OpenEMR, an open-source electronic health record (EHR) system, on four virtual hospital machines. OpenEMR is widely used for managing patient records, scheduling, billing, and clinical workflows. Its open-source nature makes it cost-effective and highly customizable, especially beneficial for small or resource-limited healthcare settings. While it lacks the robust support of commercial systems and can be complex to set up, OpenEMR plays a key role in improving patient care, ensuring compliance, and driving the digital transformation of healthcare through innovation and accessibility.

These following are the steps i went through in installing OpenEMR and ensuring that it is secured

OpenEMR installation
1. Update and upgrade Ubuntu Server
2. Install necessary packages:
 Installed the LAMP stack (Linux, Apache, MySQL, PHP)
3. Create a MySQL database and user for OpenEMR:
4. Download and extract OpenEMR:
5. Configure Apache: 
6. Complete OpenEMR installation via the web-based setup.

 Steps  used in securing OpenEMR on virtual machine using Ubuntu server
1.	Update and upgrade Ubuntu Server:
2.	 Enable automatic security updates
3.	 Configure a firewall:
4.	 Secure Apache:
5.	Restart Apache:
6.	Ensure that all user accounts within OpenEMR have strong, unique passwords to reduce the risk of unauthorized
access.
7.	 Keep OpenEMR up to date

   Below are the screenshots of the OpenEMR for each of the four hospitals:
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/17abaf4be15d4ef08b271e43f5156866481b1407/Screenshot%202025-02-17%20131505.png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/535b13f6f8063ed10efc09d3b78bd3f625c08a6e/Screenshot%202025-02-17%20131940.png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/f5a7ea77bd1d1a9906429b9c69cb5c44974d2aaa/Screenshot%202025-02-17%20132154.png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/21ed4e5269e69c3a13f53aded900efa345642237/Screenshot%202025-02-17%20132546.png)

   # Architecture Development Part 3:Generation of Synthea Patient and Syndromic Surveillance Data for Hospital EHRS to Stimulate Disease Outbreak
   I used Synthea to generate synthetic patient data for simulating disease outbreaks. It helps test EHR systems and public health responses without using real patient data. While not as complex as real-world data, it’s a valuable, privacy-safe tool for outbreak modeling and healthcare system testing.
   The following are the steps i undretook in the development of this architecture:
   
1. Installed Synthea
2. Downloaded the latest version of Synthea from the official GitHub repository
3. Created a directory for Synthea and move the JAR file
4. Generated disease Simulation Message on the Synthea directory
   Below are the pictorial evidence of my work.
   
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/743bea00dba68ffd36c808ea11ec38516eb32b9c/Screenshot%202025-04-17%20232305.png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/05bd0fb169ccc8995812a94ff6bdf3a5dd0c4252/Aspirus%20Hospital%20(1).png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/ca7d687b5a6a2c7d68b1fd8b12ae9edfdcf0db67/Baraga%20Hospital%20(1).png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/e6137d1056f04afad6e3667773d6c706e404b367/Marquette%20Hospital.png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/342897377c65ddda2f171546e212d7d74bd1425f/Portage%20Hospital.png)

   # Architecture Development Part 4: Installation and Configuration of Hapi-FHIR Server
   This project i  installed and configured a Hapi-FHIR server, an open-source tool based on the FHIR standard for secure healthcare data exchange. Hapi-FHIR supports interoperability and real-time sharing of health information, crucial for public health monitoring and outbreak response. While it offers flexibility and collaboration benefits, it requires investment in training and infrastructure. Overall, Hapi-FHIR helps improve data-driven decision-making and enhances coordination during public health emergencies.
   I went through the following steps in installation and configuartion:
   
 1.	Logged in into UPHIE VM
   
 2.	Ensured docker is running
   
 3.	Installed HAPI FHIR
    
 4.	Fetched the Latest HAPI FHIR Image
   
 5.	 Configuration via the overridden application.yaml file
    
 6.	 Deployed Docker Container
   
Below is the installed Hapi-FHIR server

![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/7b36121e4fc55f98245349b94e5869add7b50042/hapifhir.png)

# Architecture Development Part 5: Interoperability-FHIR Data Exchange with HAPI-FHIR
This explores how Hapi-FHIR is used to accept and process HL7 FHIR messages for public health surveillance. With it, I can pull key data like patient info, lab results, and clinical observations from EHRs in real time. This helps public health teams track outbreaks faster and make informed decisions to protect population health.
 steps:
 1.	Installed POSTMAN
 2.	Logged in to HAPI-FHIR Virtual Machine
 3.	CRUD Operations using HAPI FHIR REST API
 4.	Created a New Practitioner
 5.	Searched for Practitioner instances
 6.	Searched with Conditions
 7.	HAPI FHIR Dashboard
 8.	Python REST API
    ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/7ed61f961089e8030ccd522b72aae7a349643c65/response.code.png)

    # Architecture Development Part 6:Aggregation and Visualization of Data for Disease Outbreak Surveillance
   	This involves aggregating FHIR-based patient data from four hospitals to support real-time public health analytics. The goal is to help health professionals and the public make informed decisions through clear visualizations. This work aids in outbreak detection, resource planning, public awareness, and evidence-based policymaking to improve health outcomes.

    steps involved
1.	Collect FHIR-based .json files
2.	Understand the FHIR structure
3.	 3.Write a Python script to aggregate the data
4.	Convert the aggregated data to CSV format
5.	Upload CSV files to Google Looker Studio
 6.Create Visualization
 7. Real-time functionality enabled for Google Looker studio to refresh every 15 minutes
    


    

    

   

   



