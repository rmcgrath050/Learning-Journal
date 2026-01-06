

### Lession 1 - An introduction to algorithmic thinking

- Browsing history insights: Algorithms analyse your virtual trail—what you have clicked, searched for, and lingered on. Based on this, they suggest products customised to your taste.

- Collaborative filtering: Ever noticed those 'Customers who bought this also bought…' recommendations? That’s collaborative filtering. It groups users with similar tastes and suggests items based on what others like you enjoyed.

- Content-based filtering: Algorithms examine product features. If you’re a sci-fi fan, they will recommend more sci-fi books. It’s like having a personal shopping assistant who knows your preferences.

- Matrix factorisation: Behind the scenes, algorithms break down your preferences into mathematical matrices. These matrices predict what you might like next

### Search Engines
- Ranking web pages: Algorithms analyse pages, considering keywords, links, and user behaviour. The famous PageRank algorithm, courtesy of Google’s founders, ranks pages based on authority and relevance
  
- Efficient retrieval: Imagine searching for 'best pizza places.' Algorithms zip through billions of web pages, fetching the most relevant results in a flash

<br>
Put simply: Algorithmic thinking enables efficient problem-solving by breaking down complex tasks into manageable steps.
<br> 


Sorting algorithms arrange elements in a specific order (usually ascending or descending). Here are a few notable sorting algorithms: 
- Bubble sort , comparing each element to the former and swapping
- quick sort, take an element at random,  keep splitting into groups 
- Merge sort, spilt into two sorted groups but merge them together in a sorted manner

<br>
Design algorithms, such as Dijkstra’s algorithm, to find optimal solutions. These algorithms help solve the problem with minimal effort, akin to finding the most efficient path to a destination. 

<br>
In essence, algorithmic thinking is a systematic approach to solving problems. 
It involves breaking down problems, designing efficient algorithms, and implementing these algorithms in code. 
<br>
<br>
<br>
<img width="774" height="564" alt="image" src="https://github.com/user-attachments/assets/76f1d86e-337a-489e-8b47-b37168b4d8a0" />

<br>

### Lession 2 - Software development tools and techniques

#### Tools
In data engineering, software development tools are like a craftsman’s workshop. They enable efficient project management and collaboration, helping data engineers track progress, automate processes, and enhance productivity throughout the development lifecycle. 
<br>
For example, Apache Hadoop is a popular tool for processing large datasets, while Apache Airflow is used for scheduling and monitoring workflows.
<br>

#### Version Control
Version control systems are essential in data engineering. They allow teams to manage changes to source code, enabling collaboration, history tracking, and seamless merging of code changes. 

For instance, when developing a new feature for a data processing pipeline, a data engineer can create a separate branch in Git, make changes, and then merge those changes back into the main codebase without disrupting the work of others.

<br>

#### Debugging
A critical aspect of data engineering. Common bugs include syntax errors (like typos), logic errors (where code produces incorrect results), and null pointer exceptions.
Tools like IDEs and debuggers help data engineers locate and resolve these issues efficiently.

#### Testing
It ensures that software components work as intended. For instance, a data engineer might write unit tests for individual functions or modules in their code, ensuring that each part works correctly in isolation. 
Integration testing then checks that these parts work together correctly. In test-driven development (TDD), data engineers write tests before writing the code itself, ensuring that the code meets its requirements from the outset


#### Documnetation 

Documentation in software development is akin to a blueprint in architecture. It provides a detailed overview of the software, including its design, functionalities, and operation.
This is particularly crucial when the software is complex or when multiple developers are working on the same project. 

<b>Tools </b> <br>
- Markdown: A lightweight markup language with plain-text-formatting syntax. It is often used for formatting readme files, or for writing messages in online discussion forums, and in text editors for the quick creation of rich text documents
Sphinx: A tool that makes it easy to create intelligent and beautiful documentation. It was originally created for the Python documentation

- Javadoc: The Javadoc tool parses the declarations and documentation comments in a set of Java source files and produces a set of HTML pages describing the classes, interfaces, constructors, methods, and fields


### Lession 3 - Constructing Algorithms 

Similarly, algorithms have time complexities—some are fast (constant time), while others take longer (linear, quadratic, or worse). So we aim for efficient algorithms that minimise the time needed to solve problems.

Similarly, we design algorithms to handle large datasets efficiently.

Just like engineers reinforce bridges with strong materials, we reinforce our algorithms with smart design choices.
<br> 


### Three Key techniques 
- Divide and conquer - Imagine breaking a big problem into smaller, manageable pieces. Divide and conquer algorithms recursively solve subproblems and combine their solutions. Examples include Merge Sort, Quick Sort, and binary search.
- Dynamic programming: Imagine a painter covering a canvas with intricate patterns. Dynamic programming breaks complex problems into overlapping subproblems. We store solutions to subproblems and build up to the final solution. Examples include the Fibonacci sequence and solving shortest path problems.
- Greedy Algorithms: Imagine a squirrel collecting nuts for winter. Greedy algorithms make locally optimal choices at each step. They don’t always guarantee the best global solution but work well for certain problems. An example is Dijkstra’s algorithm for finding the shortest path.

<br>
<img width="760" height="618" alt="image" src="https://github.com/user-attachments/assets/7211842a-8fe5-49fa-98d5-a669cd68081d" />

### Lession 4  - advanced techniques

Graphs are powerful tools used to model complex systems. They are like interconnected cities on a map. In this section, we will delve into advanced graph algorithms that help us navigate these ‘cities’ efficiently. 
