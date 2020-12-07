# :star2:Templates:
  - A Django template is a text document or a Python string marked-up using the Django template language. Some constructs are recognized and interpreted by the template engine. The main ones are variables and tags. A template is rendered with a context.
  - A Django relies on the render function and the Django Template language.
## The Render Function:
  - **render()** Combines a given template with a given context dictionary and returns an HttpResponse object with that rendered text.
  - The Three Parameters in the Render Function:
      -  **Requests** - The initial Request
      -  **The path to the template** - path relative to the TEMPLATE_DIRS option in the project settings.py variables.
      -  **Dictionary of parameters** - A dictionary that contains all variables needed in the template.
## Django Template Language (DTL):
  - Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable to those used to working with HTML.
    - Displaying Variables:
    
      - Variable- Syntax: {{variable}}
      - Example For Displaying Variable  by using DataTime function
      ```sh
      <html>
   
      <body>
      Hello World!!!<p>Today is {{today}}</p>
      </body>
   
      </html>
      ```
    - Changes in View
      ```sh
      def hello(request):
      today = datetime.datetime.now().date()
      return render(request, "hello.html", {"today" : today})
      ```
      
