# helloworld-react-flask-devops

1. First create a github repo(i.e hello world flask) and clone it to your local machine
2. open a terminal and check python version/update as required and then create v env
	commands: python3 -m venv venv # Create the virtual env named venv
                  source venv/bin/activate # Activate the virtual env
3. install flask using pip install flask and then create a file named app.py
4. write your hello world flask code and mention route, port and then run it using python app.py
5. go to localhost/<port> and you will see the web page running
6. Install pytest and write a test.py script. Then run it using pytest test.py
7. FOr code pep8 code standard, install flask and run flake8 --exclude venv # Ignore files in venv for quality check
8. Create a Docker file and write the folllowing command in it
FROM python:3.11.5
COPY app.py test.py /app/
WORKDIR /app
RUN pip install flask pytest flake8 # This downloads all the dependencies
CMD ["python", "app.py"]

Then in the terminal type docker build -t flask-hello-world .
then type docker run -it -p <port>:<port> flask-hello-world
then type docker run -it flask-hello-world pytest test.py
lastly type docker run -it flask-hello-world flake8

9. Now do the follwoing cmmands 
	git add .
	git commit -m "Add flask hello world application, test cases and dockerfile"
	git push origin main


