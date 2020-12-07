# :star2: Creating Virtual Environment For Windows:
  - **Step 1**: Create new directories for projects in Command Prompt:
  ```sh
  mkdir projects
  cd projects
  ```
  - **Step 2**:venv command creates the virtual environment. Activate it with the activate.bat script:
  ```sh
  python -m venv venv
  venv\Scripts\activate.bat
  ```
# :star2: Creating Virtual Environment For Mac OS:
  - **Step 1**:Create new directories for projects in terminal
   ```sh
  mkdir projects
  cd projects
  ```
  - **Step 2**:venv command creates the virtual environment. Activate it using the source command:

    
  ```sh
  python3 -m venv venv
  source venv/bin/activate
  ```
  source command reads and executes commands from a file.
  
# :star2: Creating Virtual Environment For UNIX/Linux:
  - **Step 1**: Create new directories for projects in Terminal:
  ```sh
  mkdir projects
  cd projects
  ```
  - **Step 2**:venv command creates the virtual environment. Activate it with the source command:
 
  ```sh
  sudo apt-get install python3-venv
  python -m venv venv
  source venv\bin\activate
  ```
  source command reads and executes commands from a file.
