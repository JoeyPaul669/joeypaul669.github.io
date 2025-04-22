# Claude Artifacts
>[!Note][Anthropic official documentation on Artifacts](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them)
> Artifacts allow Claude to share substantial, standalone content with you in a dedicated window separate from the main conversation. Artifacts make it easy to work with significant pieces of content that you may want to modify, build upon, or reference later.
> 
<!--**<span style="background: linear-gradient(in oklch longer hue 90deg, oklch(0.68 0.1379 0), oklch(0.68 0.1379 360)); background-clip: text; color: rgb(0 0 0 / 0)">it's okay to slay</span>** -->

## What are Artifacts?
Artifacts are a feature built into the website for the large language model (LLM) Claude. They allow Claude to generate content beyond simple chat messages that show up separate from the conversation, perfect for uses that require specific formatting or visuals. Some examples include webpages, diagrams and charts, and formatted documents.

While Claude is geared towards coding and writing applications, almost anyone can take advantage of it's tools, even if you have minimal-to-no coding experience. This guide is intended for those with minimal coding skills or anyone who may be curious about what Claude can do for them in their day-to-day life. While Claude does provide documentation and general information detailing how Artifacts work, they use technical language that assumes you have a higher base-line knowledge of LLMs than most people. This guide is an attempt to explain in accessible terms how you can utilize Artifacts and what features may suit your needs best. 

## Guide Outline

* [General Artifact Features](#General-Artifact-Features)
* [Coding Uses](#Coding-Uses)
* [Data Visualization](#Data-Visualization)
* [Document Templates](#Document-Templates)
* [Ethical Implications](#Ethical-Implications)


<!---![a](https://cincinnatizoo.org/wp-content/uploads/2016/05/tamandua-scaled.jpg)
that's all you need to know. guide over. tamandua win --->


## General Artifact Features
>![Example Artifact window showing React code for a to-do list](https://hackmd.io/_uploads/BJbzSKtTyx.png)
> An example Artifact window showcasing the code for a "simple to-do list using React"
### Preview/Code Toggle
In the top left of the example Artifact window you will see a toggle for the options "Preview" and "Code" (the eyeball and the ```</>``` respectively). It allows you to either see the code Claude has generated or the visual components created by the code. Depending on your use case, no visuals may need to be displayed, so the toggle will not appear. This is mainly when generating certain types of code. 

### Copy and Download
In the top right of the example Artifact window, a "Copy" button with a drop down menu for downloading the Artifact is displayed. 

"Copy " allows you to copy the Artifact code/content to your clipboard so that you can paste it wherever you may need. 

"Download as ..." will turn the Artifact content into a file and download it to your device. The file type depends on what Claude generated; for example, a document template might create a Markdown file while code for a program in the language C will generate as a `.c` file.

### Publish
The publish tool makes your Artifact publicly-accessible. It won't make the conversation public, but those with the public link (generated when published) will be able to view your Artifact in their browser. It cannot be edited directly from this public link, but it can be "Remixed", allowing any user to create their own Claude conversation with the Artifact. Any published Artifact must be republished to show up-to-date changes and can also be unpublished at any time. 

### Claude's Analysis Tool
The Analysis Tool allows Claude to run code that processes, analyzes, and provides real-time visualizations of submitted data. This allows users to work alongside Claude to generate Artifacts for more specific coding needs, especially for data visualization or document formatting. The analysis tool can be enabled through user settings under the "Profile" tab under "Feature Preview".


## Types of Artifacts
Claude is primarily known for its ability to generate code for a variety of use cases. 
|Type|Use Cases|
|-|-|
|**Code** |Functions and algorithms|
|**Markdown**|Document templates (guides, reports, etc.)|
|**HTML**|Web pages and user interface design|
|**Mermaid**|Diagrams and charts|
|**React**|User interface components and data visualization

## Coding Uses
>Artifact types: React, Code, HTML

One common use case for Claude is generating code, without needing to know anything about programming yourself! In Artifacts, Claude can generate React code, which is used to create interactive interfaces that run directly in your browser. These are essentially mini apps that can range from calculators and visualizers to fun things like small games and personality tests.

As an example of what Claude can do with coding, we'll go over the process of creating a tool that calculates the unit prices for different products and tells you which one has the best value.

### Getting Familiar With The Tools
Before diving into a full project, try making a small Artifact to get used to the Claude interface. In the chat box, type **"Make a small tool that multiplies two numbers from my input."** Once it's done generating, you should see an Artifact like the one below:
![Claude window showing the conversation that generated an Artifact](https://hackmd.io/_uploads/SJGJBKKTJx.png)
Feel free to test it out and ask follow-up questions before moving on.

### Creating a Unit Price Calculator
Let's say you're shopping and you want to buy some cookies. You have plenty of options, but you can't tell which has the cheapest price per cookie. Luckily, Claude can make you an Artifact for that exact purpose! By the end of this example, Claude will generate the code seen on the left of the image below, which corresponds to the artifact on the right.
![A screenshot of the Claude Artifact interface. The left shows the code for the artifact, and the right shows the preview of the Artifact from the code.](https://hackmd.io/_uploads/Bks7mTfCyg.png)


#### 1. Single Item Calculator
In a new Claude chat, type **"Create a calculator where I can enter the quantity and price for a product and automatically get the price per item."** Including "quantity and price" tells Claude exactly what you want to put in, and "price per item" tells Claude how you want the output. With that information, it should produce an Artifact like this:
![Screenshot of the Claude interface showing an artifact titled "Price Per Item Calculator". It has fields to input quantity and total price, a calculate button, and an area where it shows the calculated price per item.](https://hackmd.io/_uploads/Bk2ejKFaJg.png)
With this, you can calculate the unit price of a single product.

#### 2. Multiple Items
Now, we'll ask Claude to modify the Artifact to work with multiple products at the same time. In the same chat, type **"Add the ability to add more than one product and calculate the price per item for each of them."** Claude will modify the Artifact like this:
![Screenshot of the Claude interface showing the calculator artifact with multiple items and a button to add new items](https://hackmd.io/_uploads/HyAA6tKpJg.png)
In this new version, you can add and remove products just like we wanted to. Claude also made it possible to change the name of products, so you know exactly which ones you're looking at. However, it still requires you to click calculate for each individual product, which can get annoying. Let's get Claude to fix that.

#### 3. Removing Individual Calculate Buttons
Instead of having a calculate button for each product, it would be easier if there was one button that calculated everything. Type **"Combine the calculate buttons into one calculate button that works for every product."**
![Screenshot of the Claude interface showing the calculator artifact that has been modified with a "Calculate All Prices" button](https://hackmd.io/_uploads/rkl5Olqta1x.png)
Success! Now you only have to click the calculate button once after you change the products.

#### 4. Comparing Unit Prices
For our last update, let's make the calculator highlight the product with the lowest unit so we know which one to buy.
![Screenshot of the Claude interface showing the calculator artifact with two products, "Vanilla Dream" and "Chocolate Nightmare". Vanilla Dream has a price per item of \$0.53 and Chocolate Nightmare has a price per item of \$0.50. Chocolate Nightmare is highlighted green with the label "BEST VALUE".](https://hackmd.io/_uploads/SyVdphGRyg.png)
Now we see that buying Chocolate Nightmare is the best value, since it's $0.50 per cookie compared to $0.53 per cookie.

### Next Steps
Although this unit price calculator is all we intended to create, there's no reason you have to stop here. Maybe you want the calculator to convert units so it works with weight or volume, or change the design to a cookie theme. Experiment with any ideas you think of, and you may be surprised at what you can create. 

## Data Visualization
>Artifact Types: Mermaid, HTML, React, SVG

>[!Note] **Note**
**Ensure the Analysis Tool is enabled to allow Claude to analyze the documents you have submitted.**

Claude is able to process and organize data in various formats such as flowcharts and documents. While Artifacts may consist of code skeletons for a user to edit manually, Claude can also interpret given data and return a more detailed code blocks for specific needs.

When prompted, Claude can generate Artifacts in formats such as HTML and SVG, and can also generate code to be used specifically in tools and interfaces such as React and Mermaid. This creates more generic code blocks that can be used for general outlines that are easy to edit and build on, even without prior coding experience.
|Code|Preview (in Claude)|
|:-:|:-:|
| ![Artifact "code" window showing code fron an SVG diagram](https://hackmd.io/_uploads/ryd7SFtpkx.png) | ![Artifact "preview" window showing an SVG diagram](https://hackmd.io/_uploads/rk_mBtK61g.png) |

> Claude can generate code and a preview of its code in its own Artifact preview.

Additionally, when Claude is given custom documentation of details a user would like to include in a diagram, Claude can accurately generate more detailed Artifacts tailored for the information it's given. This is best for users who have denser, more developed ideas to put into code.
|Provided Document|Preview Result|
|:-:|:-:|
|![rkLfjFF6kl](https://hackmd.io/_uploads/HyrCO6zRyx.png)|![Flowchart Artifact generated from classes document](https://hackmd.io/_uploads/SkMdntFa1l.png)

> Claude can dissect complicated documentation and format it into a mind map or flowchart as needed
## Document Templates
>Artifact Types: Markdown, HTML, Mermaid

Another feature of Artifacts is its ability to generate document templates. Classroom assignments, budget reports, _user guides_, Claude can take any context or information given and integrate it into your desired document. Unfortunately, Claude is not capable of generating Artifacts in the form of Microsoft Word documents (```.docx``` files). They can only be downloaded as Markdown (```.md```), text (```.txt```), or PDF (```.pdf```) files. Resources online can [convert markdown to word documents](https://mconverter.eu/convert/markdown/docx/). 

As an example, assume you are a engineering student in college who needs to clean up their resume before applying for summer internships. You have a current resume, but it's a little messy and you aren't really sure how to go about cleaning it up. You ask Claude "Can you generate a sample resume for an engineering student?" It may spit out an Artifact like this: 

![Sample resume Artifact with filled in information](https://hackmd.io/_uploads/B1_2YttTke.png)

This is a great start. The formatting is appealing and the organizational structure is solid. However, you aren't Alex Rodriguez and this information isn't representative of you.  To refine the document, you may want to ask something like this: "I like the layout and format, but can you take out the sample information?"

![Resume template Artifact with fillable sections](https://hackmd.io/_uploads/BkqkoKY61x.png)

Now you have a blank-slate template with the formatting preserved. From here, you have multiple options with how to proceed. You can:

* Copy the text and paste it into a word processor like Microsoft Word or Google Docs and work on it from there.
* Ask Claude to fill in certain sections of the resume with the information you provide it (projects, previous employment, skills, etc).
* Continue to change formatting until you are satisfied.
* Download the Artifact as a PDF ready to upload to applicant pages.

In just minutes you generated a usable resume that looks good to employers and can be easily modified. If your application requires it, you could also ask Claude to create a cover-letter template using your resume. This is just one of many ways you can utilize Artifacts, and specifically document templates, to increase your productivity and assist you in your day-to-day tasks. 

## Ethical Implications
With the usage of AI, the discussion of ethics is never far off. This guide is not intended to advise you on how to ethically use LLMs or other forms of artificial intelligence, but instead this section will inform you on some basic ideals/practices that should be kept in mind when using AI/LLMs.

### Never share sensitive personal information
This is a pretty standard rule of the internet. LLMs commonly use their users' conversations for training purposes, so it is important to not share sensitive information.

### Information accuracy
Information put out by an LLM is not always correct. Accuracy can vary from slightly wrong to totally misinformed, so it is important to take whatever responses you recieve with a grain of salt. Doing your own fact checking can ensure you do not fall victim to incorrect information.

### Sources of training data
The material used to train LLMs can come from a variety of sources. Sometimes, these sources are legally ambiguous due to copyright and intellectual property rights. When using an LLM, you most likely won't be able to tell where your information is coming from, so it is important to be aware of these issues.

### Environmental concerns
LLMs and data centers require a **lot** of energy to maintain. With the proliferation of AI, more and more energy will be required for upkeep. 

