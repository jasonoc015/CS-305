# CS-305

## Cleint
Artemis Financial is a financial technology company that wanted to develop some secure communication web applications.

## Vulnerabilities
Artemis was originally only using http. This protocol is completely unencrypted during transit which allows anyone sniffing packets between the cleint and the server to intercept the communications and steal sensitive data. We created a certificate which allowed us to enable https (http secure). Now, the data in transit between the cleint and the server is encrypted.

## Assessment
The most challanging part of the vulnerability assessment was getting the Spring application to boot correctly. Web applications such as this one have a ton of dependencies. This lead to dependency troubles which did not allow Spring to boot.

## Mitigation
As mentioned previously, we implemented https to encrypt traffic over the web. We also implemented a hashing algorithm that an be used to digitally verify file integrity. Lastly, we performed a code review to ensure that our source code did not have any vulnerabilites present.

## Refactoring
When I refactored the code, I used the information provided from the textbook to ensure that I had not introduced any new vulnerabilites, specifically through request injection.

## Helpful tools
The maven dependency checker was a nice tool to use. It shows you what dependencies you use and which ones have known vulnerabilities.

## Employers
I would show them a vulnerability assessment from this course. I think it would be good to show them that I have the knowledge and experience to take a project, create a dependency check, and compile a report that outlines the vulnerabilites associated with this project.
