# Using the Notebook
Notebooks are places we can enter fragments of code to execute.  

They are stored in your workspace as part of Databricks _Control Plane_, covered in later training. 

## Features of notebooks
- We can create many notebooks. 
- Each notebook can contain many separate code blocks
- Each code block has its own editor window
- Code blocks run in order, top to bottom
- Each code block can be in any supported language

We shall be using Python and SQL throughout this course.

If you have used [Jupyter Notebooks](https://jupyter.org/) before, the Databricks notebook will be familiar to you.

## Naming the notebook
It's easier to navigate multiple notebooks if we name them

I've called this one _Playground_, rather optimistically perhaps.

To change the name, click inside the name field and type your new name:

![Renamed notebook view](/images/renamed-notebook.png)

## Using Python
At the top of the window is a grey text area, with the all-too-tempting _Start typing_ phrase.

Type in the historic

```python
print("Hello notebook world")
```

then click the _Run_ button - the blue down arrow at the top left:

![Run the Python code](/images/attempt-run-python.png)

__Oh dear!__ computer says no:

![Error message saying we have no compute yet](/images/no-compute-resource.png)
We need to select a _Compute Resource_.

## Select a compute resource
Click the blue _Go to Compute_ button.

You'll see the selection screen for the various compute options we have. These are the cloud based computers that will run Databricks and our Notebook code. There are many options, each with different price-performance and specialisms. 

We're going to use Databricks in its lowest-power (and so lowest-cost) mode.

To do this:
- Select _Single Node_
- Use _30 minutes_ as the timeout

The screen should look like this after those changes:

![Compute settings screen for single node, 30 minute timeout](/images/compute-settings.png)

Click _Create Compute_ to action those changes.

And then wait ...

It can take some time - maybe several minutes - for the resources to spin up. Patience, as they say, is a virtue ;)

## Hello notebook world!
The workspace connects to our compute resource, and for a short time, you will see a notification popup that tells you this.

The Python code will then run, and display its heart-warming output below the notebook:

![Notebook with output](/images/hello-notebook-world.png)

## Adding notes using markdown
Notebooks can contain blocks of notes written in github markdown language. 

To do this, we need to add a new code editor - and this is not particularly obvious.

![popup code and text buttons](/images/code-text-hover.png)

To add a new editor:
- Hover the cursor underneath the existing code block
- Two popup buttons appear _+ Code_ and _+ Text_
- Click on _+ Text_

This should add a new editor in the notebook. Inside the editor, add the following markdown text:

![Markdown entry](/images/text-entry.png)

Once we click outside of the editor block, the view changes. The editor is hiiden, and the markdown is rendered:

![Rendered markdown](/images/markdown.png)

We can further edit the markdown by clicking inside the rendering. the editor block will return.

## Using SQL in the same notebook
We can add a separate code block written in SQL.

Add another new editor block and type in this simple SQL query:

```sql
SELECT COUNT(1)
```

Click the Run button. After a short time, we will see the results table:

![Showing SQL query results in a table](/images/sql-results.png)

You can see a hint at the bottom of that table. It says that the results have been stored in a variable named `_sqldf`. That's your first-fix-free introduction to Apache Spark programming, which we will take the briefest of looks at next.

# Next
[Apache Spark](/spark.md)

[Back to Contents](/contents.md)
