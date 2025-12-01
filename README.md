# Yan Khonski

- [linkedin](https://www.linkedin.com/in/yan-khonski/)
- [stackoverflow](https://stackoverflow.com/users/1839360/yan-khonski)
- [github](https://github.com/yan-khonski-it)

## Senior Software Engineer, G10 - Cisco

[Secure Network Analytics](https://www.cisco.com/site/us/en/products/security/security-analytics/secure-network-analytics/index.html)

_14 August 2023 - December 31 2025_
I was laid off.

Added [Zeek telemetry](https://blogs.cisco.com/security/network-visibility-module-zeek-detections-in-secure-network-analytics) ingestion and processing 
to the SNA storage platform, expanding detection capabilities and improving network threat visibility.

Designed and implemented a 32 TB performance benchmarking pipeline testing encoding
strategies and sustaining 100k+ records/sec ingest throughput, providing data-driven insight into Zeek telemetry behavior in production workloads.

Interviewed candidates for Tech Lead and Senior Software Engineer positions.

Owned and executed major Vertica DB upgrade cycles (v11 to v23 and v25), 
including identification and resolution of upgrade-blocking defects. 
Delivered patches to internal scripts, disabled incompatible new features, and fixed log rotation failures.

Upgraded the platform from Java 11 to Java 21, modernizing dependencies (HikariCP, JDBC drivers) and resolving library conflicts and flaky tests.

Improved QA automation pipeline efficiency and delivery velocity, 
reducing pull-request approval time from several days to same-day reviews and increasing throughput to 5+ PRs/day per engineer
by introducing structured engineering practices (small, focused changes; clean code; refactoring standards).

Enabled shift-left testing by extending automation to run on feature branches, enabling custom regression runs on demand and early defect detection.

Sustained productivity of the whole team after layoffs by optimizing priorities 
and continuing to support automation PR reviews, preventing slowdown despite a reduced team.

Tech stack:
- VerticaDB
- MongoDB
- Java
- Python
- Spring Framework
- Bash
- Docker
- C (a little)


## Senior Software Engineer, L64 - Microsoft

_1 March 2022 – 31 May 2023_

Led and executed the migration of Microsoft Orleans from v3.1.7 to the latest release, including risk assessment, rollback strategy, 
and end-to-end migration planning. Ramp-ed up on the .NET/Orleans ecosystem within four weeks (transitioning from Java background).

Resolved cross-datacenter service discovery issues that initially prevented services from communicating during migration, restoring full cluster visibility.

Fixed compatibility issues introduced by changes in ID generation algorithms, adding automated tests to guarantee ID consistency and prevent data corruption.

Successfully deployed to production, validating correct service discovery and data integrity.

Migrated Orleans from 3.1.7 to the latest version.

> Details
Services (silos) can run jobs, and any job with given key can be run at most once at any moment of time.
Orleans promises that the data is not corrupted (modified concurrently by different instances of services).
Solved problems with services communication (clustering – gossip communication in the same datacenter;
multi-clustering – gossip communication of services in different datacenters) – at the beginning of migration services could not discover each other.
Finally, deployed to production and tested the correctness (services discover each other, data is not corrupted).
More details and problems I had to solve https://github.com/yan-khonski-it/orleans-migration-experience/blob/main/README.md

Resolved 60+ incidents during on call weeks, deployed a hotfix, created tasks to address false alarms. All this during my two months of work.

Tech stack:
- Azure
- Azure Traffic Manager
- CosmosDB
- .NET
- Orleans


## Principal Software Engineer – Wrike

https://www.wrike.com/

_1 January 2022 – 28 February 2023_

Internally moved to Wrike after Citrix restructuring (lay off) at the end of 2021.

Reduced the number of queries on the database by 10 %,
while our DAU grew by 2 % during Q1 2022. Analyzed most frequently executed queries, added caches (distributed, local, layered),
found and got removed unnecessary functionality with extra load,
and changed the logic to reduce the number of calls.

Resolved production incidents. An example, we had 3000 request per minute for one public API end-point 
from one customer. As it turned out, the end-point would invoke a database query,
which timeout the client request, so the client would retry.
Added rate limiter for our public API end-points based on customers plans and user settings.

Tech stack:

- Java 11, Java 17, Spring, MyBatis
- PostgreSQL
- Redis, internal caches (Guava)
- JMS (RabbitMQ)
- Kafka


## Principal Software Engineer – Citrix

https://docs.citrix.com/en-us/citrix-microapps.html

_1 September 2020 – December 31 2021_
I was laid off.

Designed, wrote architecture concept, documented (diagrams.net, confluence) 
"multi-tenant migration of job processing nodes".
Organized meetings with related teams, split the problem into manageable tasks and assigned them to the teams (and
people).

Problem:
The monolith code base was single tenant application.
We had thousands of cloud instances (each tenant required multiple instances for high availability). The motivation was
to reduce the running cost.

We decided to migrate the job processing functionality to make it multi-tenant and scalable. The next step would be to
migrate the rest functionality.
Result: during my implementation phase, Citrix laid off its employees of the whole business unit...

Previous tasks.

Fixed: performance issues (Hibernate N + 1 problem, re-wrote the code to use more efficient queries),
distributed deadlock (database update and cache update waiting for each other!).

Fixed build pipeline issues, flaky tests.

Increased test coverage of business logic (and inspired other do so) from 60 to 90 % for some modules.
Added contract (Pact) tests. Added configuration tests which ensures that configuration and properties files are valid
and application can work.

Convinced other developers to fix circular dependencies of software components.

Implemented centralized configuration (before different parts of configuration were stored in many places: environment
variables, database, command line arguments).

Tech stack:

- Java 11, Spring, Hibernate, MyBatis
- MS SQL
- Redis, internal caches (Caffeine)
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

Owned development of our platform consisting of different services written in different tech stacks (Java, .NET, Python,
PHP).

Mentored people and conducted knowledge transfers, made lectures for the company (topics: Kafka, services integration,
etc).

Fixed stability issues, memory leaks, made performance optimization (example N + 1 problem in database),
refactored poor-quality code into easy to read, tested and documented code.

Fixed problems which caused data loss and data inconsistency between services.
Examples: improper transactions handling, backward compatibility issues with messaging.

Improved REST API for some services (made it more client oriented instead of database entities oriented).
Wrote full regression REST API tests for some components (jMeter).

Tech stack:

- Java 11, Spring Boot (with Apache Tomcat embedded)
- MySQL
- MongoDB
- Kafka
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
- CSS, HTML, Javascript
- MySQL

Minor stack:

- Python3, Django, MySQL, Apache Web Server, Windows Server 2012

## Java Developer - ITA Minsk

https://www.ita-dev.com/?lang=en

_Previous years`*` - 18 November 2016_

Prototyped functionality and features, so our customer could better understand how the software will work in the future,
provided technical advise to the customer.

Automated manual process of filling data (NDA for this project, sorry):

1. Wrote a web scroller with a parser that fetches information from the internet.
2. Wrote a processor that converts the information into our business records.
3. Optimized storing those business records into the database.
4. Added a UI application to fetch and display those records to the user.

Fun project (I wanted to visualize our code base and show it to the team):
wrote a tool that builds an oriented graph representing classes (Spring Beans) dependencies of the source code
directory.

Tech stack:

- Java 8, Swing, Hibernate, Spring, ZK
- CSS, HTML, Javascript
- Yandex Maps, Google Maps API
- MySQL
- Apache Tomcat
- Windows Server 2012

## Junior Java Developer - Exadel

https://exadel.com/

_Previous years`*`_

Worked on internal and clients projects (Real estate domain, REIT).

Tech stack:

- Java, Hibernate, Spring
- CSS, HTML, Javascript
- Yandex Maps, Google Maps API
- PostgreSQL
- Apache Tomcat

## Education - Belarusian State University

### Faculty of Applied Mathematics and Computer Science

_Previous years`*`, September 2ABC - July 2XYZ_

> Previous years`*` - I do not want companies to discriminate candidates based on age.

Math and Computer Science degree 5 years (between Bachelor and Master)

Math, more math, and even more math. Played chess tournaments. Had a good time!
