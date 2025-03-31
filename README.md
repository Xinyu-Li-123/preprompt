## What is this document

This is a collection of predefined prompts to provide to LLM. The format is below

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