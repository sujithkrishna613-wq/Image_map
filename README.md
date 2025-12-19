# Ex03 Places Around Me
# Date:02-12-2025
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
```
map.html

{% load static %}
<html>
    <head>
        <title>SUJITH KRISHNA C</title>
         
    </head>
    <body>
        <center><h1>SUJITH KRISHNA C (25018114)</h1>
<img src="{% static 'map.png'%}" usemap="#image-map"></center>

<map name="image-map">
            <area alt="PERAMBUR" title="PERAMBUR" href="peram.html" coords="1017,14,1463,288" shape="rect">
            <area alt="ANNA NAGAR" title="ANNA NAGAR" href="anna.html" coords="822,486,1052,607" shape="rect">
            <area alt="KILPAUK" title="KILPAUK" href="kil.html" coords="1163,463,1492,647" shape="rect">
            <area alt="PULIANTHOPE" title="PULIANTHOPE" href="puli.html" coords="1412,242,1800,515" shape="rect">
            </map>
        
        
    </body>
</html>
```
```
peram.html

{% load static %}
<html>
    <head>
        <title>PERAMBUR CHURCH</title>
    </head>
    <body bgcolor="purple">
        
       <center>
        <img src="{% static 'peram.jpg'%}" width="70%" height="50%">
        <h1>Our Lady of Lourdes Shrine</h1></center>
        <h4>In Perambur, Chennai, the most prominent religious site is the Our Lady of Lourdes Shrine, a significant pilgrimage destination often referred to simply as the Lourdes Church, which was built as a detailed replica of the famous Basilica in Lourdes, France. Originally established as a chapel in 1880, it expanded over the decades into the large two-storied structure seen today, managed by the Salesians of Don Bosco congregation since 1934. The church hosts daily morning and evening masses, with an expanded schedule on Sundays including English and Tamil services, and it observes the 11th of every month as a special Marian Day for pilgrims, culminating in its main annual feast on February 11th. Besides this primary shrine, Perambur is home to other well-established Christian institutions like the CSI Wesley Church and the CSI Holy Cross Church on Siruvallur High Road, and St. Joseph's Syro Malabar Catholic Church on Madhavaram High Road, catering to diverse local congregations.</h4>
      
    </body>
</html>
```
```
anna.html

{% load static %}
<html>
    <head>
        <title>ANNA NAGAR</title>
    </head>

    <body bgcolor="blue">
         
        <center>
            <img src="{% static 'kora.jpg'%}" width="70%" height="50%">
        <h1>KORA FOOD STREET</h1> </center>
        <h4>Kora Food Street in Anna Nagar is a vibrant, popular food destination known for its unique concept of a modern street food market, bringing together a vast selection of local and international cuisines in a lively environment. This unique eatery is constructed entirely from re-fashioned shipping containers and is one of the city's primary spots for a late-night dining experience, open nearly 24 hours a day.</h4>
        

 
    </body>
</html>
```
```
kil.html

{% load static %}
<html>
    <head>
        <title>KILPAUK</title>
    </head>

    <body bgcolor="PINK">
       
        <center>
             <img src="{% static 'imh.jpg'%}" width="70%" height="50%"> 
        <h1>INSTITUTE OF MENTAL HEALTH</h1> </center>
        <h4>The Institute of Mental Health (IMH) in Kilpauk, Chennai, is one of the oldest and largest psychiatric care facilities in Asia. Originally established by the East India Company around 1795 as a house for "persons of unsound mind," it later came under British colonial rule and eventually evolved into the modern facility it is today. The hospital is situated on a sprawling 66-acre campus on Medavakkam Tank Road and provides a wide range of services to both inpatients and outpatients.</h4>
        

 
    </body>
</html>
```
```
puli.html

{% load static %}
<html>
    <head>
        <title>PULIANTHOPE</title>
    </head>

    <body bgcolor="yellow">
         
        <center>
            <img src="{% static 'alpha.jpg'%}" width="70%" height="50%">
        <h1>ALFA BRIYANI CENTER</h1> </center>
        <h4>The AGN Alfa Biryani Center in Pulianthope is a renowned, highly popular biryani shop famous for its affordable, flavorful South Indian and Chinese cuisine. The restaurant, located near Binny Mills on Dr. Ambedkar College Road, attracts a significant crowd, especially for its late-night and early morning offerings, and has become a local institution known for its potent flavors and pocket-friendly pricing.</h4>
        

 
    </body>
</html>
```
```
views.py

from django.shortcuts import render,HttpResponse
def fun(request):
    return render(request,'map.html')
def per(request):
    return render(request,'peram.html')
def anna(request):
    return render(request,'anna.html')
def kil(request):
    return render(request,'kil.html')
def puli(request):
    return render(request,'puli.html')
```
```
ulrs.py

from django.contrib import admin
from django.urls import path
from mapapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.fun),
    path('peram',views.per),
    path('kora',views.anna),
    path('kil',views.kil),
    path('puli',views.puli),
```
# OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/895dc407-957d-4423-9698-9c940c4c9565" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0ec04b13-123e-4396-a857-6be91b48204d" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8ec717f1-7171-4de3-8d8c-2a45fc6353ef" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b223a311-9f39-4937-a0d8-f78a1cc4a11e" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9e9ba317-b5a7-488b-b534-ecfde8017f38" />


# RESULT
The program for implementing image maps using HTML is executed successfully.
