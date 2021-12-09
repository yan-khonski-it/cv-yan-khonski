# Yan Khonski

- +420 732 455 665
- [yankhonskiy@yandex.ru](yankhonskiy@yandex.ru)
- [stackoverflow](https://stackoverflow.com/users/1839360/yan-khonski)
- [github](https://github.com/yan-khonski-it)

## Principal Software Engineer – Citrix
https://docs.citrix.com/en-us/citrix-microapps.html

_1 September 2020 – Present_

Took ownership of multi-tenant migration of job processing nodes.
Designed, wrote architecture concept of the solution, documented it (diagrams.net, confluence).
Organized meetings with related teams, split the problem into managable tasks and assigned them to the teams (and people).

Problem: 
The monolith code base was single tenant application.
We had thousands of cloud instances (each tenant required multiple instances for high availability). The motivation was to reduce the running cost.

We decided to migrate the job processing functinoality to make it multi-tenant and scalable. The next step would be to migrate the rest functionality.
Resut: during my implementation phase, Citrix laid off its employees of the whole business unit...

Previous tasks.

Fixed: performance issues (Hibernate N + 1 problem, re-wrote the code to use more efficient queries), 
distributed deadlock (database update and cache update waiting for each other!).

Fixed build pipeline issues, flaky tests.

Increased test coverage of business logic (and inspired other do so) from 60 to 90 % for some modules. 
Added contract (Pact) tests. Added configuration tests which ensures that configuration and properties files are valid and application can work.

Convinced other developers to fix circular dependencies of software components.

Implemented centralized configuration (before different parts of configuration were stored in many places: environment variables, database, command line arguments).

Tech stack:
- Java 11, Spring, Hibernate, MyBatis
- MS SQL
- Redis, internal caches (Caffeine)
- JMS (ActiveMQ)
- Hashicorp Vault
- Azure cloud (service bus, event hub, compute instances, etc)
- Docker, Docker compose
- Pact (contract tests broker)
- Mockito
- Testcontainers (for integration tests that needed running MS SQL container)

minor experience:
- kubernetes, helm

## Software Developer - Kendaxa
https://emplaya.com/en

_23 January 2019 – 31 August 2020_

Owned development of our platform consisting of different services written in different tech stacks (Java, .NET, Python, PHP).

Mentored people and conducted knowledge transfers, made lectures for the company (topics: Kafka, services integration, etc).

Fixed stability issues, memory leaks, made performance optimization (example N + 1 problem in database), 
refactored poor-quality code into easy to read, tested and documented code.

Fixed problems which caused data loss and data inconsistency between services. 
Examples: improper transactions handling, backward compatibility issues with messaging.

Improved REST API for some services (made it more client oriented instead of database entities oriented). 
Wrote full regression REST API tests for some components (jMeter).

Convinced a team to use outbox architecture pattern instead of distributed transactions
(benefits: scalability, we did not need to use distributed transaction manager, drawback - a bit of coding).

Tech stack:
- Java 11, Spring Boot (with Apache Tomcaqt embedded)
- MySQL
- MongoDB
- Kafka
- Docker Compose, Ansible, HA Proxy, Traeffic
- Spring Cloud (Service discovery Eureka, Configuration Service, Gateway).
- Groovy, Spock

## Software Engineer - CA Technologies
The company was bought by Broadcom

https://www.broadcom.com/products/software/continuous-testing/service-virtualization

_2 May 2017 - 30 September 2018_

Fixed a number of defects and bugs (some of them were critical) which improved customers’ satisfaction.

Led a group of smart interns (10 students) who built a system (wellness and benefits, event reservation for employees). 
Helped them with Architecture, deployments and hosting.

Tech stack:
- Java 8, Spring
- CSS, HTLM, Javascript
- MySQL

Minor stack:
- Python3, Django, MySQL, Apache Web Server, Windowns Server 2012

## Java Developer - ITA Minsk
https://www.ita-dev.com/?lang=en

_20 January 2015 - 18 November 2016_

Prototyped functionality and features, so our customer could better understand how the software will work in the future, provided technical advise to the customer. 
Result, the customer agreed with the solution (a project for Standard Bank).

Automated manual process of filling data (NDA for this project, sorry):
1. Wrote a web scroller with a parser that stores geographical information.
2. Wrote revere-geocoding tool to retrieve cadastrial information.
I used OpenStreet API, Nominatum, Overpass. Then I stored this information into MySQL database. Jsoup for parsing.

Fun project (I wanted to visualize our code base and show it to the team):
wrote a tool that builds an oriented graph representing classes (Spring Beans) dependencies of the source code directory.

Tech stack:
- Java 8, Swing, Hibernate, Spring, ZK
- CSS, HTLM, Javascript
- Yandex Maps, Google Maps API
- MySQL
- Apache Tomcat
- Windows Server 2012

## Junior Java Developer - Exadel
https://exadel.com/

_October 2012 - July 2013_

Worked on internal and clients projects (Real estate domain, REIT).

Tech stack:
- Java, Hibernate, Spring 
- CSS, HTLM, Javascript
- Yandex Maps, Google Maps API
- PostgreSQL
- Apache Tomcat

## Education - Belarussian State University
### Faculty of Applied Mathematics and Computer Science
_Septmeber 2010 - July 2015_

Math and Computer Science degree 5 years (between Bachelor and Master)

Math, more math, and even more math. Played chess tournaments. Had a good time!