### Rasa Entity Annontator
A simple entity annontation tool to annotate the given entities into Rasa Markdown format. It will search for given entities into each line of text file and convert it into markdown format. It is quite helpful in preparing training dataset.

**Input data format**:

```
Book me a flight from Chandigarh to New York for tomorrow.
List all available jobs in Google.
Please show me available openings in IBM.
Show me jobs available for the role data scientist.
Provide me with jobs available for the software developer role.
```

**Define entities**:

```
entities = {
    'location': ['delhi', 'chandigarh', 'mumbai', 'bangalore'],
    'book_time': ['today', 'tomorrow', 'yesterday'] # just example
    'organization': ['google', 'ibm', 'enterprisedb']
    'role': ['data scientist', 'software developer', 'qa']
}
```

**Output**:

```
- book me a flight from [chandigarh](location) to [new york]](location) for [tomorrow](book_time).
- list all available jobs in [google](organization).
- please show me available openings in [ibm](organization).
- show me jobs available for the role [data scientist](role).
- provide me with jobs available for the [software developer](role) role.
```

**TODO**:
- Add support for regex e.g regex for annotating mobile and email address
- and many more