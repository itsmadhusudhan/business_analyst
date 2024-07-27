# SQL Analyst

Analyze the sql schema and generates sql queries. I wanted to analyse llms capabilities to understand, reason and generate sql queries.

I have used `llama3.1` to generate sql queries. `llama3.1` was able to generate valid queries in most cases.

The schema that I gave as prompt is not very complex and doesn't have many tables.

It was really super fun working with `llama3.1` and generating sql queries. I feel Propmting the model is like teaching an intelligent child what is right and what is wrong.

## Thoughts(27th July 2024)

1. I took an office schema and tried to generate sql queries using llms.
2. I have repeatedly refined the prompt with aim of making llm to not make any assumptions when generating sql queries.
3. I gave ambiguous prompt to see how llm behaves like `fetch the salaries of each department` where I didn't specify whether to fetch the average salaries of employees in all departments or sum of salaries in a department.
4. Most of the generated sql queries were valid
5. LLM tend to make assumptions of not provided with enough information
6. When ambiguous prompt is given, I asked llm to ask for clarification and to not assume anything. With this llm started asking for more clarity and at the same time generating queries for different cases.
7. I believe if the sql schema passed contains metadata that clarifies the relationships between tables, then llm can generate more accurate sql queries.
8. If we want to make this usable by business people then I believe it should be multi step process where llm asks for more information and then generates the sql queries.
9. Another thing is consistency in the response. I think that can be achived by fine tuning the model and providing the model with necessary context.


## Attributions
- Schema from [https://github.com/datacharmer/test_db/tree/master](https://github.com/datacharmer/test_db)

## LICENSE
This work is licensed under the Creative Commons Attribution-Share Alike 3.0 Unported License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/3.0/ or send a letter to Creative Commons, 171 Second Street, Suite 300, San Francisco, California, 94105, USA.