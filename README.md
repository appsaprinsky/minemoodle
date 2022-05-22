# minemoodle

## Description:
This is a repository created to describe in detail the application and usage of my new project, that is hosted here: https://minemoodle.pythonanywhere.com/.

## What are the features?
There are possibilities to create multiple accounts with multiple roles. For regular users there are 3 main roles: owner, teacher, student. One additional role for developers (admin).
Users (owners) can create new subjects (modules), upload multiple resources to there (files that could be downloaded and viewed by other users), create new grades for teachers, add teachers and students to modules and even change passwords for every user (that is pinned to a particular University). However, there are restrictions for the owner role: he could only modify resources, modules and users that are part of a particular University, where the owner holds full control (the name of the role owner describes it ideally = OWNER of UNIVERSITY).
Users (teachers) have only limited control: control over modules they are participating in, grades to students and change only their own Password. 
Users (students) could only view their modules, resources to those modules and their grades.

## URL Patterns:
```
urlpatterns for all users = [  path(''),   path('signup/student/),   path('signup/teacher/'), path('signup/owner/'),         
   path('login/'),  path('logout/'),   path('change-password/'), ]

urlpatterns for owners = [  path('dashboard/'), path('modules/list/'), path('modules/list/old/'),      
     path('modules/create/'),  path('modules/view/<int:pk>/'),  path('modules/update/<int:pk>/'),            
     path('modules/delete/<int:pk>/'), 

     path('modules/view/<int:pk>/resources/create/'), path('modules/view/<int:pk1>/resources/view/<int:pk>/'),     
     path('modules/view/<int:pk1>/resources/update/<int:pk>/'), 
     path('modules/view/<int:pk1>/resources/delete/<int:pk>/',),

     path('modules/view/<int:pk1>/resources/view/<int:pk2>/file/create/'), 
     path('modules/view/<int:pk1>/resources/view/<int:pk2>/file/update/<int:pk>/'), 
     path('modules/view/<int:pk1>/resources/view/<int:pk2>/file/delete/<int:pk>/'), 

     path('grades/list/'), path('grades/create/'),  path('grades/view/<int:pk>/'),  path('grades/update/<int:pk>/'),  
     path('grades/delete/<int:pk>/'),  path('teacher/list/'),  path('teacher/list/old/'), path('teacher/create/'), 
     path('teacher/view/<int:pk>/'),  path('teacher/update/<int:pk>/'),  path('teacher/delete/<int:pk>/'), 

     path('student/list/'),   path('student/list/old/'), path('student/create/'),  path('student/view/<int:pk>/'), 
     path('student/update/<int:pk>/'), path('student/delete/<int:pk>/'),  path('user/update/<int:pk>/), ]




urlpatterns for teachers = [ path('dashboard/'),  path('modules/view/<int:pk>/'),  
    path('modules/view/<int:pk>/resources/create/'), path('modules/view/<int:pk1>/resources/view/<int:pk>/'),     
    path('modules/view/<int:pk1>/resources/update/<int:pk>/'), 
    path('modules/view/<int:pk1>/resources/delete/<int:pk>/'), 
    path('modules/view/<int:pk1>/resources/view/<int:pk2>/file/create/'), 
    path('modules/view/<int:pk1>/resources/view/<int:pk2>/file/update/<int:pk>/'), 
    path('modules/view/<int:pk1>/resources/view/<int:pk2>/file/delete/<int:pk>/'),  
    path('grades/list/'),  path('grades/create/'), path('grades/view/<int:pk>/'),  
    path('grades/update/<int:pk>/'),  path('grades/delete/<int:pk>/'),  path('student/update/<int:pk>/'),]

urlpatterns for students = [ path('dashboard/'),  path('modules/view/<int:pk>/'),  
    path('modules/view/<int:pk1>/resources/view/<int:pk>/'),  path('grades/list/'),  ]


```


## Examples of Website UI (from the owner point of view).

images/1a.png














## How to test it?


owner1
username: owner1
email: owner1@gmail.com
password: DummyPassword


teacher1
username: teacher1
email: teacher1@gmail.com
password: DummyPassword

student1
username: student1
email: student1@gmail.com
password: DummyPassword

Just follow the Url Patterns or intuitive UI design for understanding.


## Technologies used:
HTML, CSS, BOOTSTRAP 5, Django, Django Templates, Pythonanywhere.

