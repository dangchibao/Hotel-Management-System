				HOTEL MANAGEMENT SYSTEM GUIDLINE
B1:
git clone https://github.com/dangchibao/Hotel-Management-System.git

B2:Run command in Window PowerShell:

pip install Django==3.1.4

pip install django-phonenumber-field[phonenumbers]

B3:Move to file HMS and Run command:

cd HMS
python3 manage.py shell
from django.contrib.auth.models import Group, User
from accounts.models import Employee
Group.objects.create(name='admin')
Group.objects.create(name='manager')
Group.objects.create(name='receptionist')
Group.objects.create(name='staff')
Group.objects.create(name='guest')
user = User.createuser=User.objects.create_user('admin', password='admin123')
group = Group.objects.get(name="admin")
user.groups.add(group)
admin = Employee(user=user, salary=0)
admin.save()

B4:Start a new Window PowerShell.Run command:

cd HMS
python3 manage.py makemigrations
python3 manage.py migrate

B5:Run command:

python3 manage.py runserver

#### Note : If you have run the project next time, you only need to do B5

* Login in to the system with username by admin: "admin" and password : "admin123"
* Login in to the system with username by guest: click Sign up

