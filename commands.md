# Snepet commands

```bash
    snepet --add # Add a snippet using Q/A
    snepet --add --language=java --prefix="prefix" --name="name" --body="code" # Explicitly adding a snippet
    snepet --add --language="java" --global # Creates a global snippet
    snepet --add . # Adds a snippet that is only scoped to that project
    snepet --get --language="java" --index=10 # Get a snippet using the language and index
    snepet --get --id="@java:10" # Get the snippet using its id
    snepet --get --all # Get all the snepets for all languages
    snepet --get --all --language="java"
    snepet --get --all . # Gets the snippets only for the current project
    snepet --get --all --language="java" # Gets all the java snippets that belong to the current project
    snepet --update --language="java" --index=10 # Updates the stated snippet
    snepet --update --id="@java:10" # Same as creating a new snippet but ovverides
    snepet --delete --language="java" --index=10 # Deletes the snippet
    snepet --delete --id="@java:10" #Deletes the snippet
    snepet --delete --all --lanuage="java" # Deletes all the snippets
```
