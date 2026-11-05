**10/31/26**<br>
**MPAD2003A & Introductory Data Storytelling**<br>
**Carlos & Valdez**<br>
**Presented to Jean-Sébastien Marier**<br>

# Deliverable 2: Exploratory Data Analysis (EDA)

# Official Bilingualism Vs. Everyday Reality: Language Barriers in Ottawa Healthcare

## Foreword

This exploratory data analysis examines the structural and demographic distribution of non-official language speakers across Ottawa's municipal wards using the City of Ottawa's 2021 Long Form Census Ward Dataset.  Building on my initial story pitch, this report demonstrates whether local health equity and community health services keep pace with the city's rapidly diversifying multilingual neighbourhoods; specifically focusing on key wards such as Rideau-Vanier and Somerset.

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## 1. Getting Data

For my exploratory analysis, I have selected the 2021 Long Form Census Ward Dataset published on [Open Ottawa].  (https://open.ottawa.ca/datasets/ottawa::2021-long-form-census-ward-data/about)

Currently, to import this data into Google sheets, I downloaded the raw .csv file directly from their portal.  Next, I imported the file into sheets, using "Replace spreadsheet" to populate the rows.  The imported dataset can be accessed via my [Public Google Sheets Spreadsheet]  (https://docs.google.com/spreadsheets/d/1frPs9xn0qgetXE0PTjPqiEm5rBZTXNIspGW2AnpYdj8/edit?usp=sharing)

![Google Sheets Screenshot](longformcensus.png)<br>
*Figure 1: The Imported 2021 Long Form Census Dataset in Google Sheets.*

### General & Specific Observations

In total there are 2,603 rows and 26 columns in this dataset, I'd say overall the data looks clean enough.  
It is a lot to look at though and puts strain on my eyes, so to effectively visualize this data I will be only selecting and comparing relevant columns & rows given a posed question/depending on the angle I am exploring.

A few key variables I've noticed in Column A specifically, featuring discrete and continuous numerical variables representing aggregated census values for each specific Ward in Ottawa include: 
    
    - Rows tracking household sizes represent discrete numerical variables tracking counts of private households. (e.g. 2 persons, 3 persons)
    - Rows tracking financial metrics represent continuous numerical variables capturing monetary amounts. (e.g. Median monthly shelter cost, Average value of dwelling)
    - Rows tracking percentages represent continuous ratio variables measured as precentages. (e.g. % of owner households in core need)

## Out of the Ordinary Observations to Note:

I have noticed rows and specific cells showing '0' or ellipses (...) depending on data suppression rules applied by Statistics Canada to protect privacy in low population dissemination areas or specific wards.

### Potential Hypothesis:

Despite Ottawa's official bilingual designation, the rapid growth of non-official mother tongues led by Arabic and Mandarin highlights a shifting linguistic landscape that challenges traditional bilingual service delivery in certain municipal wards.  

**Here are examples of functions and lines of code put in grey boxes:**

1. If you name a function, put it between "angled" quotation marks like this: `IMPORTHTML`.
1. If you want to include the entire line of code, do the same thing, albeit with your entire code: `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternatively, you can put your code in an independent box using the template below:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
This also shows how to create an ordered list. Simply put `1.` before each item.

## 2. Understanding Data

### 2.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

### VIMO Analysis

To instill this data's reliability and analytical integrity, this dataset was audited using the VIMO framework (Validity, Integrity, Completeness, and Accuracy).  Assessing these angles has become essential before mapping or visualizing the data, as undetected errors can lead to skewed insights and misleading narratives (Cairo, 2016).  Rather than auditing every variable, my evaluation focused specifically on the primary rows driving this analysis: language metrics (non-official language speakers), age demographics (seniors), and median income.  Connecting these specific data points is key to understanding how language barriers might affect access to local healthcare services.  

# Validity 

I made sure the columns had the correct format.  For instance, checking the rows listing non-official language speakers only had numbers and didn't have text errors that would mess up further visualizations for this EDA.

# Integrity 

I ensured the dataset stayed aligned across columns.  This meant keeping language and income data tied to the correct geographic wards so I didn't accidentally match one neighbourhoods language stats with another's healthcare needs.

# Completeness

I scanned the dataset for any missing information.  In rows showing non-official language speakrs or vulnerable groups, some smaller population numbers might be left blank by Statistics Canada for privacy.  I noted where data was missing so it wouldn't skew the healthcare access analytics.  

# Accuracy

I even took the initiative to double check numbers against logical totals.  As checking the data helps prevent basic mistakes.  Furthermore, I made sure the language breakdown numbers added up properly before drawing conclusions about which wards might need better multilingual health resources.  

Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As seen in Bounegru & Gray (2011), a data visualization should be clear...

### 2.2. Cleaning Data

To prepare the census dataset for healthcare equity analysis, three primary cleaning procedures were applied across the selected wards:

# Trimming Whitespace and Column Filtering

Using Google sheets built-in data cleanup tools ( Data > Data cleanup > Trim whitespace), all extra trailing and leading spaces in the category descriptions were stripped.  The primary ward columns (Columns N, P, T) and key demographic rows were then extracted into a focused tab, isolating non-official language speakers, age groups, and income levels to remove irrelevant census data.  

# Reorgranizing Text Strings with Formulas

To make ward headers and category labels cleaner for pivot table reporting, spreadsheet formulas were used.  The SPLIT function was used to isolate specific header text from raw CSV string parameters: =SPLIT(A2, ":").

The CONCENATE function was then used to merge language indicators directly with targeted ward numbers for clear chart labeling: concatenate(A5, " - Ward ", N$1).

# Standardizing Categories with Find and Replace

The find and replace tool (Ctrl + H) was used to fix messy text labels.  Abbreviated or inconsistent census text entries (such as "Non-off. lang." or "Eng/Fr Neither") were replaced with standardized terms like "Non-Official Language Speakers" and "Neither Official Language Spoken" to maintain clarity across all tables.  





### 2.3. Analyzing Data

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 3. Delivering Data

Insert text here.

## 4. References

Include a list of your references here. Please follow [APA](https://apastyle.apa.org/style-grammar-guidelines/references) or [MLA](https://www.mla.org/MLA-Style) guidelines for references. Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
