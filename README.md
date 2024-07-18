# Student Enrollment Application

This project is a Django-based web application designed for student enrollment, featuring an AJAX-powered registration form and capabilities for exporting student data to CSV and PDF formats. Additionally, it includes an admin dashboard for managing student records efficiently.

The Student Enrollment Application aims to streamline the process of registering students and managing their information. Users can register students through a user-friendly form that utilizes AJAX to submit data without refreshing the page. This application supports exporting student data to CSV and PDF formats, which is beneficial for generating reports and maintaining records in a portable and widely-used format. Furthermore, the Django admin interface provides a robust dashboard for administrators to view and manage student records with ease.

To get started with the Student Enrollment Application, you need to clone the repository from GitHub using the command `git clone https://github.com/SanjanaMadhyastha/student-enrollment.git` and navigate into the project directory with `cd student-enrollment`. It is recommended to create and activate a virtual environment for the project. You can create a virtual environment using `python -m venv myenv` and activate it with `source myenv/bin/activate` on Linux or macOS, or `myenv\Scripts\activate` on Windows. After setting up the virtual environment, install the required packages using `pip install django reportlab`.

Next, create the database and apply migrations with `python manage.py makemigrations` followed by `python manage.py migrate`. To access the admin interface, create a superuser by running `python manage.py createsuperuser` and following the prompts to set up a username and password. Finally, run the development server using `python manage.py runserver` and navigate to `http://127.0.0.1:8000/` to access the application.

The registration form can be accessed at `http://127.0.0.1:8000/enrollment/register/`. Fill in the required fields and submit the form to register a student. The form will provide immediate feedback on successful registration or any errors encountered. To export student data, visit `http://127.0.0.1:8000/enrollment/export/csv/` for CSV export or `http://127.0.0.1:8000/enrollment/export/pdf/` for PDF export. The admin interface is available at `http://127.0.0.1:8000/admin/`, where you can log in with your superuser credentials to view, edit, and manage student records.

The code structure includes `models.py` for defining the `Student` model representing student records, `forms.py` containing the `StudentForm` for handling student registration, and `views.py` which includes views for handling registration, CSV export, and PDF export. Additionally, `urls.py` maps URLs to the corresponding views, and `admin.py` registers the `Student` model with the Django admin.

If you encounter issues with student registration not reflecting in the admin dashboard, ensure that the AJAX form submission is working correctly and that the data is being saved to the database. You can check the database directly using Django's shell to confirm the entries, and verify that the `Student` model is registered correctly in the admin.

We welcome contributions to enhance the functionality and features of this project. Please fork the repository and submit pull requests for review. This project is licensed under the MIT License. See the LICENSE file for details.



