## Building QnA with watxonx.ai, watsonx assistant, and DB2
This demo showcases how knowledge from databases (specifically DB2) can be utilized. The Q&A functionality works by translating text into SQL commands in DB2 and then presenting the output as text.

Overview:
watsonx.ai unleash the power of AI to convert human natural language into SQL statement without having technical knowledge about database. Helping management and other business users to get the data in more efficient way.

In the demo you will create 3 stages:
1. Create prompt template to convert human natural language into SQL query
2. Executing SQL query directly into DB2 database
3. Create prompt template to provide answer in more engaging way

### Prompt Template: Convert Human Natural Language into SQL Query

1. Create a new prompt template
2. Create a new prompt variable called user_question
3. Open file Create prompt-convert-query-to-SQL.txt, copy and paste into your new prompt template
4. Ensure you have put user_question variable in right place, or on 2nd line before end
5. Save your prompt template as your preferred name
6. Promote it into your deployment space
7. Go to your deployment space and deploy your prompt template
8. Wait until the process has done. You will get unique endpoint like https://us-south.ml.cloud.ibm.com/ml/v1/deployments/xxx-xxx-xxx-xxx-xxx/text/generation?version=2021-05-01 when the process is successful

### Function: Execute SQL Query

1. In your project, create a new jupyter notebook asset and use notebook deployment-execute-SQL-query.ipynb as base code
2. Set APIKEY and space_id with yours
3. You will get DB2 credentials from your mentor later during incubation
4. Try to experiment with the function to see how the data looks like
5. When you have run all cells, you will get new deployment space

### Prompt Template: Provide Engaging Answer

Follow this document to complete the task
