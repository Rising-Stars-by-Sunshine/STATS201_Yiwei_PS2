# Code
## Description
- The data query process involves importing a dataset using Pandas in Python, reading a CSV file, and creating a JSON file. The code initializes an empty list for data storage, iterates through each row of the dataset, and constructs a structured output based on specific columns. This structured data is formatted into a dictionary and appended to the list. Finally, the list containing the structured data is written to a JSON file using the json.dump method. This process is language-agnostic and showcases the general steps of reading, processing, and exporting data, adaptable to languages like Java and Go with their respective syntax adjustments.
## pseudo-code
 ________________________________________________________
| Python                            | Java   | Go       |
|-----------------------------------|--------|----------|
| import pandas as pd               | // Import statements | // Import statements |
| df = pd.read_csv("Tweets.csv", engine='python', sep=None) | // Read CSV file | // Read CSV file |
| dataset_data = []                 | // Initialize data structures | // Initialize data structures |
| temp1 = len(df.text)              | // Get data length | // Get data length |
| for i in range(0, temp1):         | // Loop through data | // Loop through data |
|     temp2 = "The sentiment is " + df.sentiment[i] + ". Because of it contains " + str(df.selected_text[i]) | // Process data | // Process data |
|     dataset_data.append({"instruction": "Detect the influence of price.", | // Construct data structure | // Construct data structure |
|                          "input": df.text[i],                        | // Construct data structure | // Construct data structure |
|                          "output": temp2})                         | // Construct data structure | // Construct data structure |
| import json                       | // Import statements | // Import statements |
| with open("dataset.json", "w") as f: | // Write to JSON file | // Write to JSON file |
|     json.dump(dataset_data, f)    | // Write to JSON file | // Write to JSON file |
|___________________________________|____________________|____________|

```
\begin{table}[h]
\centering
\begin{tabular}{|p{4cm}|p{4cm}|p{4cm}|}
\hline
\textbf{Python} & \textbf{Java} & \textbf{Go} \
\hline
\texttt{import pandas as pd} & \texttt{// Import statements} & \texttt{// Import statements} \
\texttt{df = pd.read_csv("Tweets.csv", engine='python', sep=None)} & \texttt{// Read CSV file} & \texttt{// Read CSV file} \
\texttt{dataset_data = []} & \texttt{// Initialize data structures} & \texttt{// Initialize data structures} \
\texttt{temp1 = len(df.text)} & \texttt{// Get data length} & \texttt{// Get data length} \
\texttt{for i in range(0, temp1):} & \texttt{// Loop through data} & \texttt{// Loop through data} \
\texttt{\quad temp2 = "The sentiment is " + df.sentiment[i] + ". Because of it contains " + str(df.selected_text[i])} & \texttt{// Process data} & \texttt{// Process data} \
\texttt{\quad dataset_data.append({"instruction": "Detect the influence of price.",} & \texttt{// Construct data structure} & \texttt{// Construct data structure} \
\texttt{\quad\quad\quad\quad\ "input": df.text[i],} & \texttt{// Construct data structure} & \texttt{// Construct data structure} \
\texttt{\quad\quad\quad\quad\ "output": temp2})} & \texttt{// Construct data structure} & \texttt{// Construct data structure} \
\texttt{import json} & \texttt{// Import statements} & \texttt{// Import statements} \
\texttt{with open("dataset.json", "w") as f:} & \texttt{// Write to JSON file} & \texttt{// Write to JSON file} \
\texttt{\quad json.dump(dataset_data, f)} & \texttt{// Write to JSON file} & \texttt{// Write to JSON file} \
\hline
\end{tabular}
\caption{Pseudo-code for Data Query Process}
\label{table:data_query}
\end{table}
```
## Flowchart
- ![](1.png)
