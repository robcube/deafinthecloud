---
title: "Managed Workflows for Apache Airflow"
date: 2020-11-24T13:43:37-06:00
draft: false
---
See the announcement: <a href="https://aws.amazon.com/blogs/aws/introducing-amazon-managed-workflows-for-apache-airflow-mwaa/">Managed Workflows for Apache Airflow (MWAA).</a>

Let's start by asking what is Apache Airflow and why it plays an important part in automating the data flow in your business? Airflow is a standardized tool and framework that gives you visibility to your data flow end-to-end from ingestion to output (or multiple times over). It has a great graphical view showing users status of each workflow called DAG (Directed Acyclic Graphs). There are several DAGs floating around in the internet but here’s one as an example:
<img alt="Apache Airflow DAG example" src="//deafinthecloud.com/images/mwaa-dag.png" style="padding: 4px;height:240px;">
Credit: <a href="https://blog.usejournal.com/testing-in-airflow-part-1-dag-validation-tests-dag-definition-tests-and-unit-tests-2aa94970570c">blog.usejournal.com</a>

Sure, we can custom built software to build a scalable event-driven system with all the bells and whistles that allows you to react to data in real time, however, as you all know with custom software, it comes with ongoing technical debt, takes time for new people to get on-board, arguably complicated DevOps, along with a few more drawbacks. Granted, custom-built software does matches value for value of what you need done, however it develops gaps between what the business wants and what the software executes.

This is where data orchestration tools such as <a href="https://airflow.apache.org/">Apache Airflow</a>, <a href="https://www.prefect.io/">Prefect</a>, <a href="https://metaflow.org/">Metaflow</a>, <a href="hhttps://docs.celeryproject.org/en/stable/">Apache Celery</a>, <a href="https://github.com/spotify/luigi">Luigi</a>, et al, comes in. We can combine the power and flexibility of custom software to go along with a ubiquitous platform that can be used by different data science shops everywhere all using similar conceptual model; you know what to expect.

On Nov 23rd, 2020, Amazon Web Services (AWS) has announced the release of MWAA which is rated G for Everyone. _For some reason, when I see the name, I feel I’m looking at the organization behind the movie ratings, MPAA._ Puns aside, MWAA stands for Managed Workflows for Apache Airflow. Let us dissect the name: 'Managed' as in being serverless, the elixir of keeping things away from your Kubernetes folks; 'Workflow' as in tying things together which is what business is all about; 'for Apache Airflow' honoring the open source contributions of all those who developed and curated the Apache Airflow community. (Yes, you may have to thank AirBnB for contributing the initial code base of course!)

There’s some great tutorials on using Apache Airflow – because it is a “managed service” on AWS, we won’t need to pay much attention to the install and setup which can be a bear. We cannot even run Apache Airflow on Microsoft Windows boxes – tried as I might, I actually gave up. Having it on AWS eliminates that HUGE headache of where does it go and how best to put it on a stable platform while staying secure?

This is one example of a YouTube video on Airflow that I enjoyed from the Apply Data Science channel <a href="https://youtu.be/43wHwwZhJMo">YouTube</a>
The Airflow Docs has some great examples you can follow along using MWAA. Apache Airflow has community-developed plugins you may add at the server side to better integrate the service with AWS among others. With MWAA as part of your AWS organization, you have ready-to-go recipes to integrate it with S3, Athena, Lambdas, et al… Per docs you may tie it together with the following services:
<ul>
<li>AWS Batch</li>
<li>Amazon CloudWatch</li>
<li>Amazon DynamoDB</li>
<li>AWS DataSync</li>
<li>Amazon ECS</li>
<li>AWS Fargate</li>
<li>Amazon Elastic Kubernetes Service (EKS)</li>
<li>Amazon Kinesis Firehose</li>
<li>AWS Glue</li>
<li>AWS Lambda</li>
<li>Amazon Redshift</li>
<li>Amazon Simple Queue Service (SQS)</li>
<li>Amazon Simple Notification Service (SNS)</li>
</ul>

If a service on there is missing that you need integration with, provide some feedback to AWS. Given AWS's track record, that list will grow exponentially akin to features constantly being added to CloudFormation, Lambdas, EventBridge and so on.

I’m looking forward in seeing what we all can do with MWAA on AWS! I’ll have you known that this blog post doesn’t do <a href="https://airflow.apache.org/">Apache Airflow</a> itself much justice, however, take the time to explore it, kick its tires, and see if it’s a good fit for your data workflow. You won’t regret it as knowledge out of it will benefit your future architectural decisions.

Good luck!