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
7.	8. Keep OpenEMR up to date

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
   Below are the pictorial evidence of my work
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/743bea00dba68ffd36c808ea11ec38516eb32b9c/Screenshot%202025-04-17%20232305.png)
   ![](https://github.com/David5-cyber/Public-Health-Disease-Surveillance-Architecture-Development-Project/blob/05bd0fb169ccc8995812a94ff6bdf3a5dd0c4252/Aspirus%20Hospital%20(1).png)
   

   



