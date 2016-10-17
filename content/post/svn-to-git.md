+++
draft = false
title = "svn to git"
date = "2016-10-17T20:19:40+08:00"
tags = ['svn', 'git', 'subversion']
categories = ['scm']
+++

#### Guidelines to migrate:

1. You should always migrate the history.
2. Remove sensitive information in case they are accidentally committed into older repositories.
3. You should automate the migration process as well.
4. Automated migration process should happen in an isolated environment and not on developers laptop.
5. Original author should be preserved for every commit. There are multiple ways to solve. I recommend you to explore to tailor the process according to your needs.
6. Make use of Git lfs for extremely large files.
7. Do not change your existing pipelines to build the code. Rather create new pipelines for building the source code.
8. All migration scripts should be version controlled as well.

#### On "the day" of migration:

1. Aim to migrate with just 1 click.
2. Your continuous integration (ci) pipelines should start to build code from new repositories.
3. You should clearly have mechanism’s in place to differentiate artifacts from old and new pipelines.
4. Ensure you run all your tests against the generated artifacts.
5. If your test results are acceptable then open the gates for developers to commit into new repository.
6. Finally lock down your old repository.
