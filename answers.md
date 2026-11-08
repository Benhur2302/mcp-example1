# MCP Machine Learning Agent — Assignment Answers

### Question 1: How many tools did the server list in Part 1, and how many in Part 3? What did you have to change in the client to make the new tool appear?

In Part 1, the server had 8 tools. After I created the `predict_both` tool, the number increased to 9 in Part 3. I didn't need to make any special changes to the client to display the new tool. Once I added it to the server using `@server.tool()`, the client was able to find it automatically when I ran `list_tools()`.

### Question 2: On how many of the 114 test patients do the two models disagree? For each of those patients, which model was right?

I tested both models on all 114 patients and found that they disagreed on 8 patients. Logistic Regression gave the correct prediction for 7 of them, while KNN was correct for only 1 patient.

| Patient Index | Model That Predicted Correctly |
| ------------- | ------------------------------ |
| 3             | Logistic Regression            |
| 25            | Logistic Regression            |
| 48            | Logistic Regression            |
| 53            | KNN                            |
| 76            | Logistic Regression            |
| 80            | Logistic Regression            |
| 99            | Logistic Regression            |
| 102           | Logistic Regression            |

### Question 3: Overall, which model was right more often when they disagreed?

Based on my results, Logistic Regression performed better when the models disagreed. It correctly identified 7 out of the 8 patients, while KNN was correct only once. This shows that Logistic Regression gave more accurate predictions in these particular cases.

### Question 4: Why does the description in triple quotes matter when an AI app uses this tool?

The description inside the triple quotes tells an AI application what the tool is supposed to do. This is important because the application uses that information to decide when to call the tool. If the description is clear, it becomes easier for the AI application to understand the tool's purpose and use it correctly.

### Question 5: Why is it useful for the server to log every tool call?

Logging every tool call is helpful because it lets us keep track of what happened when the tools were used. We can check which tool was called, whether it worked, and if any errors occurred. In my project, the Parquet audit log helped me confirm that the `predict_both` tool ran successfully for the test patients. These logs also make it easier to find problems and review the results later.
