# EDR-Evaluation-Methodology
[![](https://img.shields.io/badge/Service-Threat%20Hunting-A43792?style=flat-square)]() [![](https://img.shields.io/badge/Category-Methodology-E5A505?style=flat-square)]() 

Nowadays Threat Hunting is a very popular term on the InfoSec community. However, there is not a consensus in the definition of this role. When it comes to our Threat Hunting model, we start everyday by assuming the hypothesis that all of our clients have been compromised somehow. From that point, we use our knowledge to query the telemetry available in the EDR solutions to refute that hypothesis. It is only when we have deemed every match as a false positive that we discard this compromise hypothesis.

EDR solutions are the weapon of choice in our model of Threat Hunting. We also aim to be agnostic to the technology and capable of integrating our service in heterogeneous client environments. Hence, it is a must for us to know those solutions that can handle our Threat Hunting model, those that can not, and the evolution of both groups over time. This project implements an ad hoc methodology for evaluating EDR solutions according to our Threat Hunting model. 

This is an alive project, and will be updated as we perform new evaluations and revisit old solutions to check for improvements.

Besides the updated version of the methodology in this repository, you can access the Google SpreadSheet Table [here](https://docs.google.com/spreadsheets/d/1fTuqEXysxNzNURoHKDjuuayd4Kyifvpp/edit?usp=sharing&ouid=101713221252055534624&rtpof=true&sd=true).

<p align="center">
  <img src="https://github.com/blackarrowsec/EDR-Evaluation-Methodology/assets/44729887/ac602bc4-73a8-48c1-b1b0-befdb60bfa96" width="960" >
</p>


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

All the code included in this project is licensed under the terms of the MIT license.

#

[![](https://img.shields.io/badge/www-blackarrow.net-E5A505?style=flat-square)](https://www.blackarrow.net) [![](https://img.shields.io/badge/twitter-@BlackArrowSec-00aced?style=flat-square&logo=twitter&logoColor=white)](https://twitter.com/BlackArrowSec) [![](https://img.shields.io/badge/linkedin-@BlackArrowSec-0084b4?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/blackarrowsec/)
