## What is this document

This is a collection of predefined prompts to provide to LLM to **start the conversation**. It's not meant to be used to continue an existing conversation.

The format is below

Name: <Name>

Description (optional): <Description>

Tags (optional): <Tag1>, <Tag2>,...

Notes (optional): <Notes>

Prompt:

```
<Prompt>
```

Such format makes it easy to search for specific prompt using regexp. For example to search for a specific tag, we could use `^Tags:.*research.*`

You could copy-and-paste the following lines to add new prompts

Name:

Description:

Tags:

Notes: 

Prompt:

```

```

### Notes

- For readability, the entire document is intentionally formatted in markdown format. As a result, the prompt is wrapped within a code block. That being said, the document is easier to work with as a plain text file using text editor like Vi or VSCode.

- For ease of use, this document is intentionally kept within a single text file instead of some form of database.

## Prompts

### Summarize a tech paper

Name: Summarize this paper

Description: A general prompt that summarize a paper hierarchically

Tags:

Notes: This prompt should be accompanied with the paper's pdf

Prompt:

```
Summarize this paper with

- one liner of TLDR
- problems & background
- key challenges & solutions
- key insights
- detailed explanation of the main contribution
  - if it's a framework, explain how it is designed, and what are the innovative design in the framework
  - if it's a model, explain how the model is defined, and the theory behind the model
  - if it's a benchmark, explain how the benchmark is designed and collected, and how it differs from existing ones.
  - if it's a critic to some other papers, explain the critic in detail
    either way, provide an example as well to explain the key contribution, best if the example is from the paper.
- future work / unsolved problems, according to the paper
- section by section summary
```

### Summarize a chapter from a tech book

Name: Summarize a chapter from a tech book

Description: A general prompt that summarize a chapter structurally

Tags:

Notes: This prompt should be accompanied with the paper's pdf

Prompt:

```
Give a study-note summary of this book chapter. Output the following:
- TL;DR
- Key concepts & designs
- Subsection-by-subsection
```

### Reliably learn a concept from a pdf file

Name: Reliably learn a concept from a pdf file

Description: Learn a concept from a pdf file reliably, because LLM can only refer to the pdf file when synthesizing its output. The key here is reliability: LLM is great resource aggregator, but when the resources themselves are bad, the output is bound to be garbage. If you provide a sole, authorative source of truth, the LLM output should be much more reliable.

Tags:

Notes: This prompt should be accompanied with a pdf of book / paper / etc.

Prompt:

```
Refer **solely** to the pdf of <enter name of pdf file(s)> attached below. And explain <question> according to solely the book's content. Explicit spell out the location within the pdf file from which you derive your explanation of the concept.
```

### Collect information from the Internet, and don't make things up

Name: Collect information from the Internet, and don't make things up

Description: ^

Tags:

Note: 

```
From the Internet, <your question>? Please cite solely from reliable sources on the Internet (from well-known forum / website, or from well-received blog posts, or from peer-reviewed / high-ref-count papers). Don't come up with your own idea from your internal knowledge. And please attach reference to each point you made.
```


### Quick tutorial on a library

Name: Quick tutorial on a library

Description: When the goal is to get familiar with a library from scratch, it's better to learn from working example than from documentation. This is what "Getting Started" section in a doc is for, but we can make it more concise with an AI prompt.

Tags:

Note: 

```
Give me a tutorial on the library <library name>. Use self-contained code snippets to cover the common usage of this library so I can be familiar with it. Add concise comments in the code to explain how features of the library work.
```
