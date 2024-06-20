# EDR-Evaluation-Methodology
[![](https://img.shields.io/badge/Service-Threat%20Hunting-A43792?style=flat-square)]() [![](https://img.shields.io/badge/Category-Methodology-E5A505?style=flat-square)]() 

Nowadays Threat Hunting is a very popular term on the InfoSec community. However, there is not a consensus in the definition of this role. When it comes to our Threat Hunting model, we start everyday by assuming the hypothesis that all of our clients have been compromised somehow. From that point, we use our knowledge to query the telemetry available in the EDR solutions to refute that hypothesis. It is only when we have deemed every match as a false positive that we discard this compromise hypothesis.

EDR solutions are the weapon of choice in our model of Threat Hunting. We also aim to be agnostic to the technology and capable of integrating our service in heterogeneous client environments. Hence, it is a must for us to know those solutions that can handle our Threat Hunting model, those that can not, and the evolution of both groups over time. This project implements an ad hoc methodology for evaluating EDR solutions according to our Threat Hunting model. 

This is an alive project, and it will be updated as we perform new evaluations and revisit old solutions to check for improvements.

<p align="center">
  <img src="https://github.com/blackarrowsec/EDR-Evaluation-Methodology/assets/44729887/ac602bc4-73a8-48c1-b1b0-befdb60bfa96" width="960" >
</p>

# Updated Evaluation Tables

**Disclaimer:** since there is no way of translating all the information included in the project's document to markdown tables, we will not be adding neither the section "Conlusions" or the comments that give context to the score of each feature. In order to access the complete project, download the last version of this repository.

**Last Updated:** 20/06/2024

## Telemetry Section

| **Telemetry Feature Category** | **Sub-Category**            | **SentinelOne (2023)**  | **Sophos (2024)** | **TrendMicro (2024)** 
|------------------------------|-----------------------------|:-----------------------:|:------------------:|:-----------------:|
| **General**                    | TTA ☠️                      | 🟩                      | 🟥                | 🟥                                                                   
|                                | TTL ☠️                      | 🟩                      | 🟨                | 🟩                                                                   
| **Linux**                      | Processes ☠️                | 🟩                      | 🟩                | 🟩                                                
|                                | Files ☠️                    | 🟩                      | 🟥                | 🟩                                      
|                                | Network ☠️                  | 🟩                      | 🟩                | 🟩                                    
|                                | Logon ☠️                    | 🟩                      | 🟩                | 🟨                                                     
|                                | Scheduled Tasks              | 🟥                       | 🟥               | 🟥                                                         
| **Windows**                    | Processes ☠️                | 🟩                      | 🟩                | 🟩                                                
|                                | Files ☠️                    | 🟩                      | 🟥                | 🟩                                       
|                                | Network ☠️                  | 🟩                      | 🟩                | 🟩                                    
|                                | Logon ☠️                    | 🟩                      | 🟩                | 🟨                
|                                | Registry ☠️                 | 🟩                      | 🟥                | 🟩               
|                                | AMSI/Dotnet                 | 🟨                      | 🟥                | 🟩               
|                                | Event Logs                  | 🟨                      | 🟨                | 🟩               
|                                | Modules ☠️                  | 🟩                     | 🟥                | 🟩               
|                                | Scheduled Tasks              | 🟩                      | 🟩                | 🟩                             

## Query Language Section

| **QL Feature Category**        | **Sub-Category**                                             | **SentinelOne (2023)**  | **Sophos (2024)**  | **TrendMicro (2024)** 
|------------------------------|--------------------------------------------------------------|:-----------------------:|:------------------:|:-----------------:|
| **General**                    | There is a feature to run hunting queries  ☠️                | 🟩                      | 🟩                | 🟩                                                                   
|                                | Query language is well documented                            | 🟨                      | 🟩                | 🟩    
|                                | Query language is potent enough to perform our hunting  ☠️   | 🟩                      | 🟩                | 🟨    

## Administrative Tools Section

| **Admin Tools Feature Category** | **Sub-Category**                                                                                | **SentinelOne (2023)**  | **Sophos (2024)** | **TrendMicro (2024)** 
|------------------------------|-------------------------------------------------------------------------------------------------|:-----------------------:|:------------------:|:-----------------:|
| **File retrieval**             | Suspicious files can be retrieved for analysis ☠️                                              | 🟨                      | 🟥                | 🟩                                                                                                                         
| **RTR**                        | The shell supports at least Windows and Linux endpoints ☠️                                       | 🟩                      | 🟩                | 🟩                                                
|                                | The shell is not command-restricted                                                             | 🟩                      | 🟩                | 🟨                                      
|                                | The shell is reliable ☠️                                                                        | 🟨                      | 🟩                | 🟩                                    
|                                | Files can be downloaded through the shell                                                        | 🟥                      | 🟥                | 🟩                                                                                                  
| **Audit**                      | The EDR offers ways of auditing the activity performed on the EDR by users ☠️                    | 🟩                      | 🟩                | 🟩                                                
| **Agents information**         | There is a panel to see the status of the agent and general information of all the hosts  ☠️     | 🟩                      | 🟩                | 🟩                                       
|                                | There are ways to retrieve all off the data necessary to create our clients reports ☠️           | 🟩                      | 🟨                | 🟨                                    
|                                | There are ways to see the App Inventory of a host                                                | 🟩                      | 🟨                | 🟩                
| **Policies**                   | Response policies can be set to specify the EDRs behaviour on different groups of hosts ☠️       | 🟩                      | 🟩                | 🟨               
|                                | Update policies can be set to specify how they should be applied                                  | 🟩                      | 🟩                | 🟨               
|                                | Remediation policies can be set to specify the EDRs behaviour on different groups of hosts ☠️     | 🟩                      | 🟩                | 🟨               
| **Integrations**               | The EDR offers native ways of integrating the reception of alerts/incidents with other platforms   | 🟩                     | 🟨                | 🟩               

## Features Section

| **Features Category**        | **Sub-Category**                                                                                | **SentinelOne (2023)**  | **Sophos (2024)** | **TrendMicro (2024)** 
|------------------------------|-------------------------------------------------------------------------------------------------|:-----------------------:|:------------------:|:-----------------:|
| **General**                  | The EDR implements a Dark Mode for its UI                                                       | 🟩                      | 🟩                | 🟩                                                                                         
|                              | The EDR implements mechanisms to create exclusions in the alerts/incidents ☠️                    | 🟨                      | 🟨                | 🟩
|                              | The EDR implements mechanisms to create exclusions in the queries results ☠️                   | 🟩                      | 🟨                | 🟩 
|                              | The EDR provides a way to retrieve quarantined files for analysis                               | 🟨                      | 🟥                | 🟩                
|                              | The EDR provides a verification of the signature of binaries                                    | 🟩                      | 🟨                | 🟩                
|                              | The EDR provides a verification of the integrity of files                                       | 🟩                      | 🟥                | 🟩                
| **External engines integration**   | The EDR is connected with VT or other external detection engines to check if a sample is well-known             | 🟥                      | 🟥                | 🟥                                                
|                                    | The EDR is connected with VT or other IP/Domain information engines to provide information about IPs/Domains    | 🟥                      | 🟥                | 🟥                                                                                                                                      
| **USB control**                | The EDR provides ways to block USBs                                                           | 🟩                      | 🟩                | 🟨                                                
|                                | The EDR provides ways to monitor the activity of USBs                                         | 🟥                      | 🟥                | 🟨                                                
| **Platforms**                  | The EDR supports Windows endpoints  ☠️                                                       | 🟩                      | 🟨                | 🟩                                       
|                                | The EDR supports Linux endpoints ☠️                                                          | 🟨                      | 🟨                | 🟩                                    
|                                | The EDR supports MacOS endpoints                                                              | 🟨                      | 🟨                | 🟩                
|                                | The EDR supports mobile endpoints (Android/iOS)                                               | 🟨                      | 🟨                | 🟩                
|                                | The EDR supports containers                                                                   | 🟨                      | 🟨                | 🟨                
|                                | The EDR supports WSL                                                                          | 🟨                      | 🟨                | 🟥                
| **Identity**                   | The EDR has identity related features                                                         | 🟩                      | 🟨                | 🟩               
|                                | Hunting can be performed on the Identity-generated telemetry                                  | 🟥                      | 🟥                | 🟩               
| **Response**                   | The EDR has automatic response features ☠️                                                    | 🟩                     | 🟩                | 🟨   
|                                | The EDR has manual response features ☠️                                                       | 🟩                     | 🟩                | 🟩   
| **Remediation**                | The EDR provides remediation capabilities                                                     | 🟩                     | 🟩                | 🟩   
| **Custom Rules**               | Custom detection rules can be created based on behaviour                                      | 🟩                     | 🟨                | 🟨   
|                                | The response actions for the triggered detection rules are enough                             | 🟩                     | 🟩                | 🟩   
| **Visibility**                 | The EDR has a panel where incidents/alerts are available with a concise but sufficient amount of information that links to a more detailed view of each cases  ☠️      | 🟩                      | 🟥                |  🟩                                      
|                                | The EDR provides a Process Tree view ☠️                                                                                                                                | 🟩                      | 🟨                | 🟩                                    
|                                | The Process Tree view is developed enough ☠️                                                                                                                           | 🟩                      | 🟨                | 🟩                
|                                | Is possible to check in the Process Tree events of different types related to the processes involved ☠️                                                                | 🟩                      | 🟨                | 🟩                
|                                | The EDR provides a timeline feature that can be used to review relevant events on a timelapse                                                                          | 🟨                      | 🟥                | 🟥                

## API Section

| **API Feature Category**        | **Sub-Category**                                                            | **SentinelOne (2023)**  | **Sophos (2024)**  | **TrendMicro (2024)** 
|---------------------------------|-----------------------------------------------------------------------------|:-----------------------:|:------------------:|:-----------------:|
| **General**                     | Is possible to perform hunting queries via API  ☠️                          | 🟩                      | 🟩                | 🟨                                                                   
|                                 | Is possible to retrieve data about the hosts, incidents and alerts via API   | 🟩                      | 🟩                | 🟩    

## UI Section

| **UI Feature Category**         | **Sub-Category**                                                                 | **SentinelOne (2023)**  | **Sophos (2024)**  | **TrendMicro (2024)** 
|---------------------------------|----------------------------------------------------------------------------------|:-----------------------:|:------------------:|:-----------------:|
| **General**                     | The UI is intuitive and easy to navigate                                         | 🟩                      | 🟥                | 🟩                                                                   
|                                 | The UI contains a panel where detailed information about a user can be checked   | 🟥                      | 🟨                | 🟥    
|                                 | The UI contains a panel where detailed information about a host can be checked   | 🟥                      | 🟨                | 🟥    


## MITRE ENGENUITY ATT&CK EVALUATIONS Section

| **Campaign**                              | **Scenario**                                                                     | **SentinelOne**  | **Sophos**  | **TrendMicro** 
|-------------------------------------------|----------------------------------------------------------------------------------|:-----------------------:|:------------------:|:-----------------:|
| **APT3 (2018)**                           | **CobaltStrike**                                                                     | 1,69%                      | N/A                | N/A              
|                                           | **PowerShell Empire**                                                                | 2,60%                      | N/A                | N/A                                                                   
| **APT29 (2020)**                          | **Scenario 1**                                                                       | 0%                      | N/A                | 10,13%    
|                                           | **Scenario 2**                                                                       | N/A                      | N/A                | 20%    
| **Carbanak+FIN7 (2021)**                  | **Carbanak**                                                                         | 85,42%                      | 20,83%                | 38,54%   
|                                           | **FIN7**                                                                             | 87,18%                      | 19,23%                | 46,15%   
| **Wizard Spider + Sandworm (2022)**       | **Wizard Spider**                                                                    | 92,31%                      | 55,77%                | 67,31%   
|                                           | **Sandworm**                                                                         | 92,98%                      | 42,11%                | 82,46%   
| **Turla (2023)**                          | **Carbon**                                                                           | 86,84%                      | 63,16%                | 43,42%   
|                                           | **Snake**                                                                            | 65,67%                      | 58,21%                | 56,72%   


Authors
---------------
Julio J. Estévez-Pereira ([@nmapcansave](https://twitter.com/nmapcansave))

Colaborators
---------------
Alberto Terceiro Plumed (alberto.terceiro@blackarrow.net)

References
---------------

* https://attackevals.mitre-engenuity.org/results/enterprise
* https://detect.fyi/edr-telemetry-project-a-comprehensive-comparison-d5ed1745384b

License
-------

All the documents included in this project are licensed under the terms of the Apache 2.0 license.

#

[![](https://img.shields.io/badge/www-blackarrow.net-E5A505?style=flat-square)](https://www.blackarrow.net) [![](https://img.shields.io/badge/twitter-@BlackArrowSec-00aced?style=flat-square&logo=twitter&logoColor=white)](https://twitter.com/BlackArrowSec) [![](https://img.shields.io/badge/linkedin-@BlackArrowSec-0084b4?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/blackarrowsec/)
