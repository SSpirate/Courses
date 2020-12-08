# :star2: Basic Tags and its Syntax:
  - Tags has ability to perform many operations such as for loop, if condition, Temporal inheritance and so on.
  - Generally tags will be like this **{% tag_name %}**. Some Tags have beginning **{% tag_name %}** and ending tags **{% endtag_name %}**.
  - <ins>**if Tag**</ins>:
      - This "if tag" operation is similar to other Programming Language such as Python.
      ```sh
      <html>
      <body>
   
      Hello World!!!<p>Today is {{today}}</p>
      We are
      {% if today.day == 1 %}
      
      the first day of month.
      {% elif today.day == 30 %}
      
      the last day of month.
      {% else %}
      
      I don't know.
      {%endif%}
      
      </body>
    </html>
      ```
  - <ins>**For Tag**</ins>
      - This  'for' tag, that works exactly like in Python. Let's change our hello view to transmit a list to our template −
      ```sh
      def hello(request):
      today = datetime.datetime.now().date()
   
       daysOfWeek = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
       return render(request, "hello.html", {"today" : today, "days_of_week" : daysOfWeek})
      ```
      - The template to display that list using {{ for }} −
      ```sh
      <html>
      <body>
      
      Hello World!!!<p>Today is {{today}}</p>
      We are
      {% if today.day == 1 %}
      
      the first day of month.
      {% elif today.day == 30 %}
      
      the last day of month.
      {% else %}
      
      I don't know.
      {%endif%}
      
      <p>
         {% for day in days_of_week %}
         {{day}}
      </p>
		
      {% endfor %}
      
      </body>
      </html>
      ```
  - Similar to these tags there are so many tags.Refer this link [**Reference**](https://docs.djangoproject.com/en/3.1/ref/templates/builtins/) for more tags.
