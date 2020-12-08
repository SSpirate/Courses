# :star2: Django-Templates:
  - Being a web framework, Django needs a convenient way to generate HTML dynamically. The most common approach relies on templates. A template contains the static parts of the desired HTML output as well as some special syntax describing how dynamic content will be inserted.
  -  Django Templates depends on the Two things:
      - **Render function.**
      - **Django Template Language(DTL).**
##   **Render Function:**
    - render() Combines a given template with a given context dictionary and returns an HttpResponse object with that rendered text.
##  **Django Template Language(DTL)**
  - <ins>**Variables:**</ins>
    - A variable outputs a value from the context, which is a dict-like object mapping keys to values.Variables are surrounded by {{ and }} like this:
       - **Syntax:**
            - ```sh
              Course done by{{ first_name }}. Course published in {{ last_name }}.
              ```
       - Here {{ first_name }} and {{ last_name }} are variables.      
    - With a context of {'first_name': 'SSpirate', 'last_name': 'GitHub'}, this template renders to:
       -  ```sh
          Course done by SSpirate. Course published in GitHub.
           ```
  - <ins>**Filters:**</ins>
      - Filters transform the values of variables and tag arguments.They help you to modify the variables at display time.
        - **Syntax:**
          - ```sh
            {{variable|filters}}
            ```
           - **Examples:**
               - ```sh 
                    {{ django|title }}
                  ``` 
            * With a context of {'django': 'this is my first course'}, this template renders to:
              * ```sh
                This Is My First Course
                ```
            * {{string|truncatewords:80}} − This filter will truncate the string, so you will see only the first 80 words.

            * {{string|lower}} − Converts the string to lowercase.

            * {{string|escape|linebreaks}} − Escapes string contents, then converts line breaks to tags.    
