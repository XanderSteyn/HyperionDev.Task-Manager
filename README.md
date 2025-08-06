<h1 align="center">
  <img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Tasks/Task%20Manager.svg" width="100%" height="130px" alt="Task Manager - CLI Task Management Application"/><br>
</h1>

<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Features.svg" alt="Features" height="25px"/>

- **User Authentication:** Secure login system with password masking
- **User Management:** Admin can register new users to the system
- **Task Management:** 
  - Add new tasks with title, description, assigned user, and due date
  - View all tasks in the system
  - View tasks assigned to the current user
  - View completed tasks (admin only)
  - Edit existing tasks (mark as complete, change due date)
  - Delete tasks (admin only)
- **Reporting System:** 
  - Generate comprehensive task overview reports
  - Generate detailed user overview reports
  - Display statistics with percentages and task counts
- **Data Persistence:** Stores data in text files (`tasks.txt`, `user.txt`)
- **Error Handling:** Robust error handling with user-friendly messages
- **Cross-Platform:** Works on Windows, macOS, and Linux

<h1></h1>

<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/How%20It%20Works.svg" alt="How It Works" height="25px"/>

### 1. User Authentication
- Upon launching, users **log in** with their username and password.
- Password input is securely **masked** to protect privacy.
- Credentials are stored in a local `user.txt` file.
- If no users exist, a default admin account (`admin`) is automatically created.

### 2. User Roles & Permissions
- **Admin users** have full system access:
  - Register new users
  - Delete tasks
  - Generate and view detailed reports
  - Perform all regular task operations
- **Regular users** can:
  - Add new tasks
  - View all tasks
  - View and edit tasks assigned specifically to them

### 3. Task Management
- Tasks are saved in `tasks.txt` and include:
  - Assigned user
  - Title & description
  - Assigned date and due date
  - Completion status
- Features include:
  - Adding new tasks with all necessary details
  - Viewing tasks:
    - All tasks in the system
    - Completed tasks (**admin only**)
    - Tasks assigned to the logged-in user
  - Editing tasks assigned to the user:
    - Mark as complete
    - Change assigned user
    - Update due date  
    *(Only if the task is not completed)*
  - Admins can delete tasks after confirmation

### 4. Reporting & Statistics (Admin Only)
- Generates two reports:
  - **Task Overview:** Totals and percentages of completed, incomplete, and overdue tasks.
  - **User Overview:** Task stats per user with completion rates.
- Reports are saved as `task_overview.txt` and `user_overview.txt`.
- Reports can be viewed directly within the application.

### 5. Data Persistence & File Handling
- User and task data are stored in text files (`user.txt` and `tasks.txt`).
- Automatically creates files with default data if missing.
- Robust error handling ensures smooth operation despite file or input issues.

### 6. User Interface
- Clear, console-based menus guide the user through the application.
- Input validation with helpful prompts ensures correct data entry.
- Screen clearing and pauses improve readability and navigation.
- Password masking implemented using the `maskpass` module for enhanced security.

<h1></h1>

<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Technologies%20Used.svg" alt="Technologies Used" height="30px"/>

- **Python** – Core programming language
- **maskpass** – For secure password input with masking
- **datetime** – Date validation and manipulation
- **Text Files** – Simple data storage (`tasks.txt`, `user.txt`)

<h2></h2>

<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/Repos/Setup%20Instructions.svg" alt="Setup Instructions" height="30px"/>

#### 1. Clone the repository
```bash
git clone https://github.com/XanderSteyn/HyperionDev.Task-Manager/
```

#### 2. Change to the project directory
```bash
cd "HyperionDev.Task-Manager"
```

#### 3. Create a virtual environment
- **Windows:**
  ```powershell
  python -m venv venv
  ```
- **macOS/Linux:**
  ```bash
  python3 -m venv venv
  ```

#### 4. Activate the virtual environment
- **Windows (Command Prompt):**
  ```cmd
  .\venv\Scripts\activate.bat
  ```
- **Windows (PowerShell):**
  ```powershell
  .\venv\Scripts\Activate.ps1
  ```
- **macOS/Linux:**
  ```bash
  source ./venv/bin/activate
  ```

#### 5. Install dependencies
```bash
pip install -r requirements.txt
```

#### 6. Run the application
```bash
python task_manager.py
```

<h1></h1>

<img src="https://github.com/XanderSteyn/xandersteyn/blob/main/IGNORE/Headers/License.svg" alt="License" height="25px"/>

This repository is protected by a custom license. See the [LICENSE](LICENSE) file for details.

Unauthorized copying or submission of this work for academic purposes is prohibited.
