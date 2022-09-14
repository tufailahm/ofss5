JAVA EE7 Training
====================


Servlets
JSP
JPA
JMS
REST Web Services
SOAP Web Services


Eclipse
MYSQL 

============================

Introduction

Name
Location
Experience and knowledge abou programming such C,C++, Java
Expectation





Eclipse
MYSQL 
https://drive.google.com/file/d/1256Cl72t_ZtJdpv4GSzsJoFPL2Y4tlTd/view?usp=sharing










Servlets
=============================================
Why ?
What ?
are java programs capable of accepting the request and sending the response 

How ?


Server Side java technology 
Response - HTML



----------------------------
Web Server



Create
Compile
Deploy in a web server
Client access it - it gets executed and response  will be sent to the client


=========================
Use case : Hi and welcome to my website


static page     -- html

dynamic page -- servlet


Use case : Personalized welcome

http://localhost:8082/product-app/login.html?username=tufail&password=12333


===============================
Lifecycle method of servlet 

init		- gets called for first request		count=100;
service		- for every request and subsequent request everytime	count++
destroy		- removing servlet from server




doGet
doPost
Servlet Chaining
==============================

RequestDispatcher



response.sendRedirect



Session Management in Servlets
==================================


http is a stateless protocol

Use case : Personalized thanks

1) HttpSession

LoginServlet
HttpSession session = request.getSession();
session.setAttribute("username",uname);


SurveyServlet
HttpSession session = request.getSession();
String uname = (String)session.getAttribute("username");


2) Cookies

Use case : You have visited for the first time or you already visited our web site.

Cookie c = new Cookie(uname,uname);
response.addCookie(c);

request.getCookies();






























3) URL Rewriting

?option=1&country=IN


4) Hidden form fields


<input type="hidden" name="favfood" value="dosa">


======================JSP

Java Server Pages

	- server side tech
	- UI



<%		%>	- JSP Scriplet and it is used to write java codes
<%!		%>	- JSP Declaration and it is used to declare variables and methods
<%--		--%>	- JSP Comments

<%= 		%>	- JSP Expression - to print/delegate the output

Create a method to generate a random number between 1 to 10 and print that number 




implicit objects in jsp

request
response
out
session
config		-ServletConfig
application	- ServletContext
error		- 


Directives
-----------------

page
taglib
include

Custom tags in JSP (Taglib)


Use case : Frequently we have to create put our signature

<signature></signature>


1. Create a class TagSupport


	doStartTag


2. Create TLD(Tag Library Descriptor) file 

	

3. Use the tags



=======

JSTL

Java Standard Tag Libaries






							Servlet
login.jsp
			submit		-->	validate if incorrect session.setAttribute("msg","incorrect username and password);
							   RequestDispacther	-	login.jsp
			


							JSP	
						validate if incorrect session.setAttribute("msg","incorrect username and password);
							<jsp:forward path="login.jsp">		
session.getAttribute("msg");

if(msg==null)
{
}
else
print(msg)




----------------------------------
Javabean/Model/POJO

properties
setter and getters


reusable component

useBean



Use case : Prompt user details and print the details


UI	page to get these details		print 
	session.setAttribute 		session.getAttribute


	<set property



Product
	productId
	productName
	quantityOnHand
	price


ServletContext 	-application

ServletConfig	- page/servlet

request		- till request is valid

session		- 



=================JPA====================================
Java Persistence API

Databases

JDBC : Problems 

Lots of lines of codes
Create tables
Manage transactions




jpa.save(product);
jpa.update(product);
jpa.get(productId);


Use case : CRUD operation on products And also we want to login/registration

DB: 


Hibernate	-JPA Framework


External libraries

























