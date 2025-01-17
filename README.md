# Auto Time Table Generation System

A web application to automatically generate optimized timetables for government schools using a **Genetic Algorithm**. The application is built with **React** for the frontend and **Django** for the backend.

## Features

- **Automated Timetable Generation**: Uses a Genetic Algorithm to create optimized timetables based on input constraints.
- **User Roles**:
  - **Administrator**: Can manage school details, teacher data, and constraints.
  - **Teachers**: View their individual timetables.
  - **Students**: Access class-specific timetables.
- **Constraint Management**: Define and manage rules like teacher availability, room allocation, and subject-specific constraints.
- **Export Timetables**: Download timetables in PDF format.

## Tech Stack

### Frontend:
- **React**: For building the user interface.
- **Axios**: For API communication.
- **Material-UI**: For responsive design and pre-styled components.

### Backend:
- **Django**: For handling requests and managing business logic.
- **Django REST Framework**: For building the RESTful API.
- **Genetic Algorithm**: Custom Python implementation for timetable generation.
- **Database**: PostgreSQL for storing application data.

## Installation

### Prerequisites:
1. **Node.js** and **npm/yarn** installed.
2. **Python 3.9+** and **pip** installed.
3. **PostgreSQL** running locally or on a cloud service.

### Backend Setup:
1. Clone the repository:

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Linux/Mac
   venv\Scripts\activate   # For Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Configure database settings in `settings.py`:
   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'django.db.backends.postgresql',
           'NAME': '<your_database_name>',
           'USER': '<your_database_user>',
           'PASSWORD': '<your_database_password>',
           'HOST': 'localhost',
           'PORT': '5432',
       }
   }
   ```
5. Apply migrations and run the server:
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

### Frontend Setup:
1. Navigate to the frontend folder:
   ```bash
   cd ../frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the React app:
   ```bash
   npm start
   ```

## Usage

### Admin:
1. Log in as an administrator.
2. Define school constraints such as teacher availability and room capacities.
3. Generate a timetable using the "Generate Timetable" button.
4. Review and publish the generated timetable.

### Teacher:
1. Log in as a teacher.
2. View your assigned timetable.

### Student:
1. Log in as a student.
2. Access your class-specific timetable.


## Genetic Algorithm Workflow
1. **Initialization**: Generate an initial population of random timetables.
2. **Fitness Evaluation**: Evaluate each timetable based on constraints like teacher availability and room capacity.
3. **Selection**: Select the fittest timetables for reproduction.
4. **Crossover**: Combine selected timetables to produce new offspring.
5. **Mutation**: Randomly alter some parts of the timetable to introduce diversity.
6. **Termination**: Repeat the above steps until the optimal timetable is found or a maximum number of iterations is reached.


## Contributing
Feel free to submit issues or pull requests. Make sure to follow the contribution guidelines.

## License
This project is licensed under the MIT License.
