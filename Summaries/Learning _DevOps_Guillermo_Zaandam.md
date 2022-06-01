# DevOps

---

## Introduction

 Hi Guillermo ,

Thanks for signing up for the OpsCentric DevOps Career Accelerator Mini Course. Once or twice a week I will send you an email outlining a DevOps skill or concept to work on and some resources or exercises for learning it.

This allows you to really solidify each skill or concept before moving on to the next one. I'm an active DevOps practitioner and consultant myself so I know what works and what doesn't.

Because I'm still an active practitioner, I stay up to date  with the latest cutting edge tech and concepts. You won't be learning any outdated crap here like you do in college or university.

I like to focus on skills and actions over credentials, so there is no certificate for completing this course. Instead I'm going to give you my personal email so you can get in touch with questions anytime.


## Lesson 1 

Hi Guillermo,

Welcome to the first lesson in the OpsCentric DevOps Career Accelerator miniseries. Today we're going to be talking about culture and its importance in the DevOps paradigm.

This may seem like an odd starting point, you are probably looking forward to the more technical content about things like like Terraform and Kubernetes. But without an understanding of DevOps culture you won't be able to get the most out of those tools.

This is because DevOps is actually a cultural phenomenon that happens to be supported by a set of tools and frameworks for automating operations. The tools are important, make no mistake about that! But culture is just as important if you want to get the most out them.

At its core DevOps is really about breaking down the barriers that traditionally existed between Development and Ops teams. Of course in real life things tend to get more complicated so it's important to remain focused on the goal, but also flexible and sensitive to the details of a given situation.

DevOps engineers tend to find themselves in one of the following situations when they are hired by a company.

The Traditional Company

A traditional company is one in which no effort has been made towards implementing DevOps yet, or an effort was made and failed leaving them effectively back at ground zero. If you are hired into a company like this you will have your work cut out for you, but you will also have a great opportunity to stand out and make an impact.

I actually love working with companies like this because you can usually identify and implement some really easy early wins and build support within the company this way. For example, a company without a CI/CD pipeline will often be amazed if you are able to take even a few of their manual build steps and automate them.

It's not always easy though, there are some very real challenges to transforming traditional companies too. The most common one you will encounter is a culture which resists change. Often traditional companies have a culture which can seem like it is terrified of any change at all.

Sometimes this can be attributed to individuals who are scared they will be obsolete and replaced by automation and sometimes it's more systemic, coming from the top of the company and manifesting itself as extreme risk aversion. In both cases the solution is the same however.

The Mid-Transformation Company

The mid transformation company is part way through a DevOps transformation. The main difference between them and a traditional company (whether they are just starting or seasoned DevOps veterans) is that there will be some level of awareness of DevOps principles and buy-in at the management level.

This doesn't mean that the company will have actually implemented DevOps effectively or that they are good at it, it just means they are trying and there is awareness. This awareness can be good but it can also be a hindrance if their idea of what DevOps is ends up being something entirely different.

If you find yourself hired into a mid-transformation company, carefully evaluate where they are really at in their transformation and their level of competence. You will then know whether you should be learning from them or trying to lead them to something better.

If you are inexperienced and find yourself in a competent company then you should learn as much as possible and support their efforts as best you can. But if you determine that they are struggling to really implement DevOps principles then it's time to step up and lead.

DevOps Leadership

You may be asking why I transitioned straight to DevOps Leadership without talking about The Transformed Company. That's because there is no such thing as a successfully transformed company. DevOps culture is not a destination it is a journey. As soon as a company thinks they have arrived at DevOps they are already falling behind. One of the most important aspects of DevOps culture is a relentless focus on continuous improvement. There is ALWAYS room for cultural and technical improvement. ALWAYS.

No matter where you are and whatever type of company you find yourself in, look for the bottlenecks. Which tools, processes or cultural practices are slowing down productive change and how can they be eliminated, improved or perfected? Note that I said productive change, not change by itself. Don't get caught in the trap of changing things for changes sake. Make sure the changes you make are actually productive.

Coming back to the 2 company types, traditional companies and struggling mid-transformation companies usually have one thing in common, a leadership vacuum. This could come from higher up within the company or be more localised to the technical side of the organisation.

Fortunately DevOps leadership does NOT require a management job title. In fact you can often get better results working from within the team instead of as a manager commanding from above. This is because of the resistance to change I mentioned earlier which is present in most people and organisations.

The way to overcome this resistance is to demonstrate a better way and make it available rather than mandating it. Adoption may be a bit slower this way but the change will last. Mandates are rarely followed once the person making them stops watching or enforcing compliance.

The better way can be technical, cultural or procedural in nature. You could help lead a blameless postmortem after a major outage to demonstrate a better way or you could automate a build process that required manual intervention previously. If you do a good job and your solution actually addresses the needs of the team it will almost always be adopted over an older suboptimal way of doing things.

If your solution is not adopted or used by the team, you will want to reevaluate whether you effectively addressed the real need. Sometimes there are hidden reasons for the way things are done which are not totally clear until you try to do away with that thing. Look at your solutions objectively and figure out where you went wrong rather than blaming the team for not using them.

Lesson One Assignment

Your assignment this week is to acquire and begin reading The Phoenix Project by Gene Kim. This book demonstrates DevOps culture in an entertaining way and I will be referring back to it for parts of this course.

You may also find it helpful to read an article I wrote previously about Subversive DevOps Leadership.

If you have questions or comments about this lesson, please feel free to email me at: cfornari@opscentric.io

Keep an eye on your inbox for lesson 2 in this series where we will talk about the big picture in DevOps and how the various types of DevOps tools work together.

---

## Lesson 2

In the last lesson we talked about DevOps culture and the 2 types of companies you will encounter during your career. This lesson expands on this theme and covers the workflows that enable a culture of continuous improvement.

The key to effective continuous improvement is choosing the right source of feedback. Without feedback it's impossible to know what needs to be improved or how much change is needed and in which direction. However if you choose the wrong source of feedback you can actually create a negative loop in which you make things WORSE with every iteration. So choose your feedback sources carefully and monitor your results frequently.

Good sources of feedback can also be stymied by incorrect actions. Think deeply about what a particular metric actually means, and the second order effects of any change you make to try and improve it. Hitting a good balance is a bit like shooting for a moving target. A change in one area will often have unintended consequences in others.

This is why it's impossible to "arrive" at DevOps completeness. It is not a destination because the target is always moving. DevOps processes mirror the real world of business and economics. They are not static and never will be, each change has unknown consequences that must be observed and corrected with further changes.

DevOps Pipelines

The backbone of the DevOps process is the pipeline. A pipeline is simply a set of actions and measurements which accomplish a goal. Measurements are the key to an effective pipeline, without them you have no idea whether you are getting better, worse or going nowhere.

One of the most common and useful DevOps pipelines is the Continuous Integration (CI) or Continuous Deployment (CD) process. In fact it could almost be said that all the other tools in the DevOps world exist to make the CI pipeline faster, more accurate and more efficient.

CI and CD are terms which can be used interchangeably but they mean slightly different things. In the days before cloud enabled Software as a Service (SaaS) software was released in slower cycles, measured in months or years not minutes, hours or days. Even with these slower cycles it was useful for software developers to receive feedback on new version faster. Thus the CI pipeline was born.

At the most basic level a CI pipeline integrates new versions of the code into the software and provides a testable version with that new code. Ideally tests are also automated and can be run with each new build, providing instant feedback to developers. Tests are one of the primary feedback loops in the DevOps world which is why writing good automated tests is so important.

A CD pipeline takes the CI pipeline to the next level and should be the ultimate goal of any DevOps enabled team. Instead of just providing feedback to developers in the form of test failures a CD pipeline actually deploys the new code to a production server or environment if no test failures are detected. CD pipelines are valuable and worth striving for because they completely eliminate human error and manual steps from the deployment pipeline, freeing up developers or DevOps practitioners to work on more productive things.

CI and CD are not the only form of pipelines in DevOps however. Another common pipeline you will encounter is an autoscaling pipeline. Autoscaling pipelines take in usage and performance data from servers and applications and perform scaling actions based on that data.

A common way to do this is to setup a server CPU utilisation metric and send that to an autoscaling process. When utilisation is low the autoscaling process can remove servers and when utilisation starts to go up the process can add new servers to handle the load.

You will find these kind of feedback loops all over in modern infrastructure once you know what to look for. They are the foundation of automated infrastructure and process.

Lesson Two Assignment

Your assignment for this lesson is to take the Jenkins guided tour, which is available here. This tour will give you a good working knowledge of Jenkins basic setup and how to create a pipeline. This will be useful for you as we move on to discussing tools in the next lesson.

If you have questions or comments about this lesson, please feel free to email me at: cfornari@opscentric.io

Keep an eye on your inbox for lesson 3 in this series where we will talk about DevOps tools and how they enable automated pipelines.

---

## Lesson 3

In the last lesson we learned about the DevOps workflow and pipelines. Now that we understand basic DevOps workflows and the feedback loops behind them, we can begin to talk about the specific tools which enable these types of automated processes. These tools can be broken down by category. I will cover each category below and the most common tools in each one.

Some of these tools are free and open source, while others are commercial. There is usually a tradeoff where free tools take longer to setup and more knowledge and time to maintain while commercial tools are easier to run and maintain but cost monthly licensing fees.

You must be guided by your teams collective knowledge of a given tool and the budget vs time tradeoffs when making a selection for any given project. When making tool selections it is tempting to think there is a "right" answer but that is almost never the case. Any tool comes with a set of pros and cons and you can only evaluate these in the context of a given project to see which one will be best for a particular situation.

CI and CD Servers

CI/CD servers detect new versions of code being pushed to your repository and take actions based on a set of rules which you can define. The most common action you would configure would be for your CI (Continuous Integration) server to pull the latest code and build > test > deploy it to a server or cloud environment. If you have implemented CD (Continuous Deployment) already then the deployment might go all the way to your production environment. If not then it would usually be deployed to a test environment for further manual verification.

I've outlined some common CI/CD server solutions below which you should begin familiarising yourself with. A future lesson will be devoted entirely to CI/CD servers and the specifics of their operation.

    Jenkins was one of the original CI/CD servers and continues to be a popular choice for many companies. It is not as easy to use or maintain as some of the commercial alternatives and many developers find it somewhat confusing. Jenkins has the benefit of a massive plugin library however and can be scripted to do virtually anything you need. This flexibility keeps it in the running despite the issues mentioned above.
    CircleCI is a fully hosted SaaS style CI solution which has gained a lot of popularity in the past few years. It uses YAML based configuration files for build definitions and the latest version is docker based. What this means is that you can build on the same docker image locally and in the CircleCI cloud eliminating many of the errors which occur in traditional server and agent based build environments. The simplicity of CircleCI does come at the cost of flexibility, it's not as configurable as Jenkins is but it covers most mainstream build and deployment needs.
    GitLab CI deserves a mention here as it's seeing rapid adoption at the moment even though total numbers still lag behind some of the more popular solutions. While it's mostly useful for those already using Gitlab it does offer a simple and easy way to deploy applications and implement CI builds.
    Azure DevOps integrates with Azure extremely well and is a strong contender especially for those building  software for windows or with the .NET framework. It has seamless integrations with Azure services and it is also more intuitive to use for developers already familiar with Microsoft products and development practices.


We'll cover some of these servers in more detail in a future lesson and give you the foundation you need to use any of them effectively.

Container Technology

Container technology falls into 2 main categories, the containers themselves and the orchestrators such as Kubernetes, Docker Swarm and ECS (Elastic Container Service). Most containers in use today are built using Docker though there are a few other formats and standards available. If you're not yet familiar with containers it's helpful to think of them as small encapsulated virtual machine images which can be run on any compatible orchestrator.

We will focus on Docker containers since they are the most widely used container today. Docker containers are defined via a file which contains instructions for adding files and installing packages in the container. In addition to containers, Docker has an orchestrator called Docker Swarm which can run their containers. However Docker Swarm is not commonly used in production deployments today. Instead most Docker Containers are deployed to Kubernetes or Amazons ECS (Elastic Container Service).

    Kubernetes is the most popular container orchestrator in use today. AWS, GCP and Azure all have Kubernetes based offerings. GKE is Google's Kubernetes offering and is very popular with developers because it tends to be quick to get started with and easy to use. AWS offers a Kubernetes based service called EKS (Elastic Kubernetes Service) in addition to their own container orchestrator ECS. Azure has a Kubernetes offering called AKS (Azure Kubernetes Service). These acronyms can get confusing, but most of them operate similarly so if you learn one you will have an easier time learning others.
    Elastic Container Service (ECS) is Amazons container offering. It's popular amongst AWS users and has 2 versions. One which you manage yourself by provisioning server instances and installing the ECS agent and a second called Fargate where you do not need to manage any instances yourself. ECS Fargate is easier to get started with but more expensive than managing your own instances in most cases.
    Docker Swarm was developed by Docker as a container orchestrator with similar features to Kubernetes and ECS. For various reasons it never saw widespread production adoption even though Docker was instrumental in the adoption of containers themselves. It's still a popular choice for developers running containers locally however. We will be covering ECS and Kubernetes later but not Docker Swarm specifically since you are unlikely to run into in a production context.


Cloud Infrastructure Automation

Cloud Infrastructure Automation tools allow cloud configuration to be stored and version controlled "as code". This means that changes to cloud environments are treated the same as changes to the application code base. The infrastructure where the application runs effectively becomes part of the application.

There are two main tools in this space in widespread use. I'll cover the benefits and drawbacks of both below.

    Terraform is an open source universal infrastructure automation tool. It uses plugins to interface with almost any cloud provider and even services like Github. It's developed and maintained by a company called Hashicorp and uses a special configuration language called HCL (HashiCorp Confirguation Language). Terraform is popular because it can be used on any cloud and makes it easier to migrate from one cloud to another if needed. Because it is open source and maintained by many people (Stewarded by Hashicorp) Terraform is usually the first to receive updates when new cloud services are rolled out and it has a huge library of plugins for almost any popular online service. 
    CloudFormation is an AWS specific tool provided by Amazon. It does a good job automating AWS infrastructure but that is the only thing it can do. Unlike Terraform CloudFormation is not open source and is maintained by AWS. This means that Terraform actually gets updates when new cloud services are rolled out faster than CloudFormation as their internal team is smaller than the open source community contributing to Terraform. CloudFormation uses YAML or JSON files for definitions which is more declarative but also less flexible than Terraform's HCL language.


Monitoring and Alerting

There are so many monitoring and alerting tools available today that it's impossible to list them all. Some are built into cloud systems such as CloudWatch on AWS and StackDriver on GCP while others like DataDog are hosted by third parties. We will cover CloudWatch, StackDriver and DataDog in later lessons, but right now it's helpful to focus on the bigger picture.

Monitoring and alerting tools ingest data coming from various sources and then aggregate, visualise and trigger alerts based on the data coming in. There are usually a few layers of data coming into a monitoring system.

    Infrastructure level data comes from servers and clusters such as Kubernetes. It will usually be statistics about utilization such as CPU, Memory or disk pace. Infrastructure level systems such as load balancers and databases also fall into this category. This data can be used to autoscale systems and generate alerts if a system is running low on resources.
    Application level data comes from the applications themselves. This is custom data defined by developers and usually sent via an SDK or library within the application itself. This data can include application performance statistics as well as utilisation numbers and even user level data at times.
    User level data is often ingested into a separate business intelligence dashboard or visualisation system instead of going to the infrastructure level monitoring system. This is because infrastructure monitoring systems are usually focused on actions and alerts over visualisation while business intelligence systems are more focused on the visualisation side of things. This is not always the case however which is why user level data is worth mentioning here. You may be called upon to send data to a separate system for visualisation while maintaining the systems for ingesting and storing it.


Logging

Logging systems receive and aggregate logs from your infrastructure and applications while providing a method to search and generate statistics about log events. There are many third party log aggregation systems each with their own strengths, but a common choice for larger companies is the ELK (Elasticache, Logstash and Kibana) stack. These components are open source and free, but do take more time to setup and run compared to commercial offerings like Splunk.

Commercial offerings tend to be quite expensive which keeps many companies running their own ELK stack or similar regardless of the amount of time it takes to setup and maintain. We will cover basic ELK stack setup in a later lesson but will not get too deep into the specifics of commercial options. Most of them have similar functionality and extensive tutorials for usage.

Lesson Three Assignment

For the last lesson assignment you learned about setting up Jenkins and pipelines. Now it's time to learn a little bit about Terraform and Cloud Infrastructure Automation.

Follow the official Terraform AWS getting started guide here: https://learn.hashicorp.com/terraform. If you do not have an AWS account. it's time to create one. You can use the free AWS tier which should not cost anything. Just be careful you don't launch anything that would be costly, and use the Terraform Destroy command to delete the resources you created when you are done.

---

## Lesson 4

Now that we've learned about DevOps Culture, Pipelines and Tools it's time to talk about the cloud. Cloud technology is one of the most misunderstood, and most important technological shifts in the last few decades. Before the cloud there were release engineers and system administrators but there was no DevOps as we know it today.

In the early days of the internet if a startup wanted to serve a website or webapp they would have to buy a physical server and place it in a datacenter somewhere with stable power and internet bandwidth available. When they got more users than the server could handle they would repeat the process and add more servers.

Buying physical servers is expensive and requires lots of upfront investment even if you only want to test an idea. It also takes specialised skills to maintain physical hardware and manage it in a reliable manner. These factors made it quite difficult and expensive to get an internet company off the ground in the days before the cloud.

Cloud technology offers a tradeoff. Pay only for what you use today, with no upfront investment but you will pay more over a longer period than if you bought a server of your own. Generally this is an excellent tradeoff for startups as they can test and validate ideas quickly and easily without being stuck paying off a server bill later on if the idea doesn't work out.

This tradeoff starts to make less sense for larger companies as they scale up. At some point it becomes cheaper and easier to run their own data centers which is why Google, FaceBook, Amazon and Microsoft all run their own infrastructure. Most of these companies even began selling capacity in their datacenters to the public in the form of cloud offerings which is how AWS (Amazon Web Services), GCP (Google Cloud Platform) and Microsoft Azure were born.

The above mentioned clouds are known as the "Big 3" public cloud offerings however there are many smaller provders offering everything from simple VPSs (Virtual Private Servers) to managed Kubernetes platforms. Hertzner, RackSpace and Digital Ocean are popular options in this category and tend to be much less expensive than the big 3 clouds but without as many tertiary services.

AWS

AWS was the original public cloud offering in the sense that we think of it today. RackSpace was available before AWS but their offerings were less streamlined and more like a colocated model then the on demand model we are now familiar with. Since AWS was the first they also tend to be the most mature and feature complete out of all the public clouds.

There are some areas where other clouds excel such as GCP with their Kubernetes offering (GKE) but in general Azure and GCP play catch up when AWS rolls out new features and services.

Since AWS is the biggest and most widely used cloud offering today I usually recommend that beginners learn it first. The knowledge you gain learning AWS will also serve you well when learning other cloud offerings.

Azure

As might be expected from a Microsoft platform, Azure excels at Windows based offerings and Enterprise. In 2019 Azure was the fastest growing cloud provider mostly due to strong enterprise adoption, though their total size is still below AWS.

Azure also has a popular CI/CD solution called Azure DevOps which has seen rapid adoption recently. If you plan to work mostly for large enterprise companies, learning Azure is a good choice. Many of Azure's offerings are similar to AWS and GCP so the concepts will transfer over even if the specifics differ.

Google Cloud

GCP is currently the smallest of the "Big 3" public cloud providers. Some of their offerings can be a bit immature or behind in features when compared to AWS but their GKE (Google Kubernetes Engine) offering is by far the best managed Kubernetes solution on the market.

AWS EKS Fargate is similar in concept but not as easy to use as GKE and it is behind on features. Azures AKS in also behind GKE making Google Cloud the go-to provider for Kubernetes based deployments. If you plan to work mostly with startups and smaller innovative companies Google Cloud is worth learning.

Digital Ocean

While it's not in the same class as the big 3 cloud providers covered above, Digital Ocean (Often referred to as DO) is worth a mention. Digital Ocean started as a provider of cheap and economical VPSs (Virtual Private Servers). They have since expanded their offerings in the cloud space including rolling out a managed Kubernetes service.

While they have less adoption than other clouds Digital Ocean is popular with startups looking to save money due to their lower prices. They also offer excellent tutorials for various sysadmin and cloud related tasks buying them further goodwill in the tech community.

Lesson Three Assignment

Your assignment this week is to install the AWS CLI which is available here. The AWS CLI allows you to create and manage AWS resources programmatically in your terminal. If you do not yet have an AWS account you should sign up for one as well at https://aws.amazon.com. You will get one year of limited free use when you sign up, which you can utilise during this course.

Once you have downloaded and installed the AWS CLI you will need to authenticate it. To do this you will need to create and AWS Access Key which can be used for command line authorisation.

Have a look here to create a new access key from the web console. Download the access key and secret as a CSV file when prompted to do so.

Once you have your access key and secret available, run this command in your terminal:

aws configure

The configure command will prompt you for the access key, secret, region and default output. Enter the Access Key ID for your credentials and the secret access key and leave the rest at defaults (us-east-1 and json).

To confirm that your access key worked and your CLI is authenticated, run the following command: 'aws ecs describe-vpcs'. You should see output indicating that no VPCs were found. If you see an error there may be a problem with the access key you configured.

You will be using the AWS CLI later in this course, so keep it installed and ready on your computer.

---

## Lesson 5

Today we are getting hands on with Docker and Docker Compose. This lesson will be a little different because it comes with a companion repository which you will need to clone to your computer.

If you do not have Git installed on your computer yet, you can find instructions to install it on Windows, MacOS and Windows here. Once you have installed Git you can run the following command to get the lesson files on your computer:

git clone git@github.com:opscentric/mini-series.git

This will copy the repository files to your computer. You should open up a terminal and navigate to the repository folder and then the docker-and-containers folder inside which contains the Dockerfile and docker-compose.yml file in addition to the test application code.

Now visit the repository README here to follow along with the lesson and get started using Docker. You will need to switch between the README and your local terminal as the lesson progresses.

The repository contains a sample NodeJS application and a Dockerfile for it as well as a Docker Compose file which will create a Postgres Database container and connect the application to it. This is an important concept in the DevOps world - connecting applications together - and it's most easily demonstrated with Docker Compose.

Later in the series you will learn a little bit about Kubernetes and how to connect real world applications together in the cloud. If you are ready to take the next step and make a commitment to your future career, enrollment for the fall semester of our DevOps masterclass is now open.

Visit https://opscentric.io to learn more and reserve your spot. I accept a very limited number of students per semester to ensure a high quality experience and I expect these spots to fill up fast. The course will cover the technologies we've been discussing in this mini-series in much more detail and includes 1 on 1 mentorship from me as you build a high paying career in DevOps.

---