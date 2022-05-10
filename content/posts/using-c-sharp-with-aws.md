---
title: "Using C# With AWS"
date: 2020-05-27T13:37:33-06:00
draft: false
---

## Introduction ##

I'm doing a series on how C# works with AWS databases. AWS has 12 different databases all under different categories. Plagarizing the chart promiently displayed on the <a href="https://aws.amazon.com/products/databases/">AWS Database page</a>, I'll go through each serverless and managed database one and see how my preferred language, <a href="https://github.com/dotnet/csharplang">C#</a>, works. If you REALLY want it done in Python too, I can do that for you.

<table>
<tr>
<th>Database Types</th>
<th>Use cases</th>
<th>AWS service</th>
</tr>
<tr>
<td><a href="#Relational">Relational</a></td>
<td>Traditional applications, ERP, CRM, e-commerce</td>
<td>Aurora, RDS, RedShift</td>
</tr>
<tr>
<td>[NoSQL](#NoSQL)</td>
<td>High-traffic web apps, e-commerce systems, gaming applications, content management, catalogs, user profiles</td>
<td>DynamoDB, DocumentDB</td>
</tr>
<tr>
<td>In-memory</td>
<td>Coming soon...</td>
<td></td>
</tr>
<tr>
<td>Wide column</td>
<td>Coming soon...</td>
<td></td>
</tr>
<tr>
<td>Graph</td>
<td>Coming soon...</td>
<td></td>
</tr>
<tr>
<td>Time series</td>
<td>Coming soon...</td>
<td></td>
</tr>
<tr>
<td>Ledger</td>
<td>Coming soon...</td>
<td></td>
</tr>
</table>

## Relational ##

<a name="Relational"></a>
Relational databases management systems (RDBMS) has been with the tech industury seemly since the beginning of time -- actually became all the rage with Ashton-Tate's dBase II in the early 80's. I remember working on my first relational database, Sybase in the late 90's, before migrating to Microsoft SQL Server 4.5. Damn, I've been around too long. The T-SQL concepts of SELECT, UPDATE, INSERT, JOINs, et al became real easy to grasp for me and millions of developers, then I fell into client-server application development with database programming as my strong suit. Relational databases still have a place in every IT shop and is arguably very dependable with plenty of people out there who are capable administrating them. 
## NoSQL ##
Now the new hotness, NoSQL -- first, throw out what you've learned about relationl databases -- just throw it out -- trust me. With NoSQL, joins should not be in your vocabulary, columns should not be in your vocabulary either, and yup, you've guessed it, rows too! The way I see it, instead of structured data, you have structured strings with each structured pieces called "attributes". Strings can be XML or JSON/BSON, or even comma-delimited if you want it to be. Most NoSQL engines are optimized for reading XML and JSON/BSON though. I see relational database vendors are shoehorning NoSQL concepts by making up JSON datatypes that works alongside your structured data. Neat concept doing that to leverage the best of both worlds, however, I don't think it <em>itching</em> feels right. Many RDMBS have XML dataypes too so adding JSON is not entirely new to database vendors. They can be interchanged to be document or key/value types -- sometimes both...

## In-memory ##

In-memory databases are the ones that are very simple key-value store and they typically reside in your server's memory rather than the disk. Memory is always faster than disk but I'm sure the differences are narrowing with ever-improving SSD speed. You can cheat a little to have a few things on disk tho' for config purposes and used as a snapshot store. You need to have things stored on disk in case of memory issues, used as a backup/restore mechanism after a clean reboot, or there might be some obscure index construct that you don't see.

## Wide column ##

This is the admittedly weird category name: wide-column. Is Cassandra considered a wide-column database or is it called a row store? It's also a key-value store but at the same time the data is stored in row store column form. Confused yet? Pfftt, moving on... If I would have to give it a category label, I would call it a 'Data Model' type database. It's like coding in the MVVM paradigm I used to build WPF and Silverlight apps: hierarchy is king. That's the way I see it in Cassandra. I'll demo it soon enough to give you a better grasp of what it looks like.

## Graph ##

Graph databases are primed to quickly show relations between two or more distinct datasets. It is primarily used showing connections within social media but there's more -- could possibly show disease vectors in real-time, maybe show relationships between individuals partaking the most basic of economic activity (hint: bartering) and seeing who came out on top, or finding correlation between exercise/practice and excelling in sports. 

## Time series ##

This is new... and still in preview form. Sign up! With the prolifteration of IoT devices (hello smart watches, tracking drivers, or letting the weather drive temperatures in your home) we need a fast way to track this huge volume of data streaming in to do further analysis. Fellow AWS Data Hero Matt White from the UK did an amazing talk on that years, err, pre-COVID ago. 

## Ledger ##

Ledger... accounting... auditing... yup, they all go together. <em>American Southern accent</em> You do an entry, then it sticks in your craw; there's no escapin'. It's Amazon Web Service's "blockchain-like" database, but it's NOT blockchain since the real blockchains are a whole different beast.

## Conclusion ##

So what's the best database technology? We never will figure this out since everyone's needs and wants are different, but it's a fun exercise exploring the differences on how we interact with the various database flavors. I hope I did a good job to show the various ways we can connect to databases and show  simple use cases for each. 

## References ##

<ul>
<li>https://aws.amazon.com/redis/</li>
<li>https://redis.io/topics/persistence</li>
<li>https://stackoverflow.com/questions/13010225/why-many-refer-to-cassandra-as-a-column-oriented-database</li>
<li>https://cwiki.apache.org/confluence/display/cassandra/DataModel</li>
<li>https://aws.amazon.com/qldb/</li>
<li>https://aws.amazon.com/dynamodb/</li>
<li>https://docs.mongodb.com/manual/tutorial/</li>
<li>https://aws.amazon.com/documentdb/</li>
</ul>
