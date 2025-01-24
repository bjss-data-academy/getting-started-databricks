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
