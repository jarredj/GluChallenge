## Programming Challenge


**Estimated time required:**
1-2 hours

**Suggested language:**
PHP

**Challenge description:**
Implement a priority queue web-api server, that can be used to add and update “jobs”
on a queue. Each job consists of a job id, submitter’s id, processor’s id (if its being
processed) and a command to execute.

The server must save the tasks in a file or database and allow for hundreds or even
thousands of job submitters and job processors to add and update jobs on the queue
simultaneously.

Job processors must be able to pick the current non-completed job with the highest
priority. No two job processors should pick the same job.

Job submitters may also be able to check the status of a job using an id that was
returned to them when they added the job to the queue. One client may be able to
submit more than one job. One job processor may only process one job at a time.

Provide a way to get current average processing time. Consider using a caching
mechanism to optimize access to the queue data. Feel free to use open source tools
and software. Prefer using composer to manage any third party libraries.

**Example End-Points:**
* POST /task Submit a new task to the queue.
* GET /task Get the next available task with highest priority.
* GET /task/$id Get the status of the task with id = $id

**What to submit:**
1. Source code
