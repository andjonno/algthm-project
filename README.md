![Algthm Logo](https://raw.githubusercontent.com/andjonno/algthm-project/master/algthm-logo.png)

algthm-project
--------------

###### Algthm Project Overview &amp; Architecture

Algthm (pronounce: _algorithm_) is an open source search engine for open source repositories. It is exists to serve developers in finding highest quality code repositories/projects that are built for a certain task. You can simply ask Algthm, what you are after and it will source you the best tool for the job.

Algthm sources code quality metrics through a number of methods. The first method is inspecting the code itself by using a number of agnostic tools such as line & file counters. This offers first level inspection. To the next level, Algthm can use language-specific tools such as linters and code complexity inspectors. And a level further, we can execute tests or pre-compile code to get very intrinsic results on the health and quality of a codebase. But Algthm's secret sauce is looking at the source of a codebase - where the code comes from - _the contributors_. Much like googles page rank algorithm (in its most simplest form) is ranking websites based on the websites they are linked from. This is super effective because it places the quality of the website by its importance factor. If a website has many websites pointing at it, then it is considered important and thus should be ranked quite highly. Obviously there are many more factors to this but this fits the purpose of Algthm and allows us to adapt this method into the open source software development world. The way Algthm ranks code-bases is primarily based on its contributors and what other projects they are contributing to. So for example, if a developer is working heavily on the highly-ranked, high-quality CodeBase A, and starts working on CodeBase B then CodeBase B's rank will start to increase quite dramatically. If a developer is committing lots of code to a high quality codebase, then this developer is considered to be highly responsible for that codebases quality. Therefore, this developers contributions carry more weight. More rank. This same weight then flows on to when they contribute to other code bases, much like in google, the rank of one website carries to the next based on its rank. So in this case, CodeBase B rank will increase by a relative factor derived from the percentage share this developer is contributing towards CodeBase A's rank... Confused? Sorry, I'll clarify this explanation another time..

* * *

### Algthm Components

There are a number of systems that make up the Algthm architecture. Here are the links to each of these projects:

* [Algthm-Crawler](https://github.com/andjonno/algthm-crawler) - Crawling Engine - sources codebases to index.
* [Algthm-Scheduler](https://github.com/andjonno/algthm-scheduler) - Schedules and distributes work across worker cluster.
* [Algthm-Dex](https://github.com/andjonno/algthm-dex) - Indexing Engine - Worker Manager; workers do labour of checking out repositories and running ranking algorithms over the code. 
* [Algthm-Search-API](https://github.com/andjonno/algthm-search-api) - Query Processor and ResultSet creation.
* [Algthm-Web](https://github.com/andjonno/algthm-web) - UI into Algthm.
 
