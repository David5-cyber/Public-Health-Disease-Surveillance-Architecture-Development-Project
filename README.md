# Public-Health-Disease-Surveillance-Architecture-Development-Project
This project simulates a regional healthcare IT architecture using virtual machines, OpenEMR, Synthea, and HAPI-FHIR to support electronic health records, disease outbreak modeling, and real-time public health surveillance. It includes VM setup, EHR deployment, synthetic data generation, FHIR-based data exchange, and dashboard visualization for COVID-19 trends across multiple hospitals

# Architecture Development Part 1: Virtual Machine Configuration/Testing
This project was focused on building a healthcare network using five virtual machines (VMs)—four representing hospitals namely;Aspirus Hospital,Portage Health,Baraga County Memorial Hospital,and Marquette General Hospital and one for the Upper Peninsula Health Information Exchange (UPHIE). The hospital VMs will run an OS compatible with OpenEMR, while the UPHIE VM will support HAPI-FHIR. All VMs  shared a common IP scheme to enable seamless connectivity and data exchange. The goal is to create a safe, controlled environment to explore health IT architecture, EMR systems, and interoperability standards like FHIR, bridging classroom concepts with real-world healthcare technology applications.

steps involved in setting up the virtual machine environment:

-Establishment of a VPN connection

-Accessed the institution's cluster

-Navigated the virtual machines

-Deployed and configured virtual marchines

-Configured all five(5) virtual machines to operate within the same IP address range and subnet

-Assigned each virtual machine to a hospital



# Architecture Development Part 2:Installation, Configuration and Security of OpenEMR
 In this project, i installed and configured OpenEMR, an open-source electronic health record (EHR) system, on four virtual hospital machines. OpenEMR is widely used for managing patient records, scheduling, billing, and clinical workflows. Its open-source nature makes it cost-effective and highly customizable, especially beneficial for small or resource-limited healthcare settings. While it lacks the robust support of commercial systems and can be complex to set up, OpenEMR plays a key role in improving patient care, ensuring compliance, and driving the digital transformation of healthcare through innovation and accessibility.

OpenEMR installation
- Updated and upgraded Ubuntu Serve
-  Installed necessary packages
-installed the LAMP stack (Linux, Apache, MySQL, PHP)
-Created a MySQL database and user for OpenEMR:
-Downloaded and extract OpenEMR
-Configured Apache 
- Completed OpenEMR installation via the web-based setup.

 Steps  used in securing OpenEMR on virtual machine using Ubuntu server
-	Updated and upgraded Ubuntu Server
-	 Enabled automatic security updates
-  Configured a firewall:
-	 Secured Apache:
- Restarted Apache:
-	Ensured that all user accounts within OpenEMR have strong, unique passwords to reduce the risk of unauthorized
access.
-	 Kept OpenEMR up to date

  

   # Architecture Development Part 3:Generation of Synthea Patient and Syndromic Surveillance Data for Hospital EHRS to Stimulate Disease Outbreak
   I used Synthea to generate synthetic patient data for simulating disease outbreaks. It helps test EHR systems and public health responses without using real patient data. While not as complex as real-world data, it’s a valuable, privacy-safe tool for outbreak modeling and healthcare system testing.
   The following are the steps i undretook in the development of this architecture:
   
- Installed Synthea
-  Downloaded the latest version of Synthea from the official GitHub repository
- Created a directory for Synthea and move the JAR file
- Generated COVID-19 Disease Simulation Message on the Synthea directory
   
   
  

   # Architecture Development Part 4: Installation and Configuration of Hapi-FHIR Server
   In this project i installed and configured a Hapi-FHIR server, an open-source tool based on the FHIR standard for secure healthcare data exchange. Hapi-FHIR supports interoperability and real-time sharing of health information, crucial for public health monitoring and outbreak response. While it offers flexibility and collaboration benefits, it requires investment in training and infrastructure. Overall, Hapi-FHIR helps improve data-driven decision-making and enhances coordination during public health emergencies.
   I went through the following steps in installation and configuartion:
   
 -	Logged in into UPHIE VM
   
 -	Ensured docker is running
   
 -	Installed HAPI FHIR
    
 -	Fetched the Latest HAPI FHIR Image
   
 -	 Configuration via the overridden application.yaml file
    
 -	 Deployed Docker Container
   


# Architecture Development Part 5: Interoperability-FHIR Data Exchange with HAPI-FHIR
This explores how Hapi-FHIR is used to accept and process HL7 FHIR messages for public health surveillance. With it, one can pull key data like patient info, lab results, and clinical observations from EHRs in real time. This helps public health teams track outbreaks faster and make informed decisions to protect population health.
 steps:
-	Installed POSTMAN
-	Logged in to HAPI-FHIR Virtual Machine
-	CRUD Operations using HAPI FHIR REST API
-	Created a New Practitioner
-	Searched for Practitioner instances
-	Searched with Conditions
-	HAPI FHIR Dashboard
-	Python REST API
    

  # Architecture Development Part 6:Aggregation and Visualization of Data for Disease Outbreak Surveillance
  
 This involves aggregating FHIR-based patient data from four hospitals to support real-time public health analytics. The goal is to help health professionals and the public make informed decisions through clear visualizations. This work aids in outbreak detection, resource planning, public awareness, and evidence-based policymaking to improve health outcomes.
 
  steps involved
-	Collect FHIR-based .json files
-	Understand the FHIR structure
-	Write a Python script to aggregate the data
-	Convert the aggregated data to CSV format
-	Upload CSV files to Google Looker Studio
-Create Visualization
- Real-time functionality enabled for Google Looker studio to refresh every 15 minutes
    

    

    

   

   



