# Advanced SIEM
## Table of Contents
1. Log Queries
2. Log Parsing
3. Operators
4. Advanced Queries
# Log Queries
- Dedicated requests
- retrieve information from SIEM
- many SIEM applications use proprietary query syntax
- many features in Splunk are based on queries
## Linux Log Queries
- Many linux logs are located in /var/log
- To display linux logs , a source must be selected : source = "log-file-path"
- the entire /var/log directory can also be viewed.
## Windows Log Queries
- source="wineventlog", displays windows logs
- sourcetype="wineventlog:[log - type] displays specifiic groups of windows logs.
## field Types
- a variety of fields can be used to filter logs.
- they are associated w/ data types, such as host, machiine data, timestamps, and others.
- splunk also supports custom fiields.
![Alt text](<../assets/field types.png>)
## Basic Wildcards
- used as placeholders in queries
- a single character can be used to retrieve data
- the * represents all and will display all logs located in /var/log.
# Log Parsing
## Parsing Overview
- SIEM parses each log added to the system.
- Parsing organzies logs into fields w/ the format [ key: value ] such as [ host: " johnd-PC']
## Parsing Methods
- Regular Expression ( Regex ) = matches a specified field value w/ an unanchored regular expression.
- Delimited = Parses fields using constant delimiters.
## Field Extraction
- Extracting maximum data from a log
- splunk may skip fields such as usernames and IPs in custom logs.![Alt text](<../assets/Field Extractiion.png>)
- Each field can be renamed according to your preference
![Alt text](<../assets/field extraction 2.png>)
# Operators
- Splunk supports logical operators
- logical operators include NOT, OR, AND.
- operators are written w/ capiital letters.
## Logical operators
- NOT = Displays the logs when the parameter is not true
- OR = Dispalys the logs if one of the parameters is true
- AND = displays teh logs only if both parameters are true
## Boolean Operators
- The query in the example below searches for access logs or error logs, iits for checking bruteforcing and etc.
![Alt text](<../assets/boolean operator.png>)
## The IN Operator
![Alt text](<../assets/the IIN Operator.png>)
- specifies the field and a list of values
## Nested Operators
![Alt text](<../assets/Nested Operators.png>)
- scenario shown above, if one condition is true, the log will be displayed
# Advanced Queries
## Advanved Syntax
- Pipe & Search = Pipe forms a chain of commands. Search is used w/ pipe to filter the output.
- AS & BY = AS renames a column, BY groups by field.
    - Splunk query syntax works w/ search processing language ( SPL) similar to SQL.

## Common Stats Functions
- Stats count ( x ) = Returns then umber of occurrences of X
- stats dc ( x ) = returns a count of the distinct value of X
- Stats count by ( x ) = Returns the number of occurrences in a specific field
## Stats Visualizatiion
- Use visualizatiion to viiew a statistiical graph.
- There are many types of graphs, including column-based, pie and bubble charts.

