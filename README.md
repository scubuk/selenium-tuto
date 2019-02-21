# Python Selenium Web Testing

## Prerequisites
* [Python 3+](https://www.python.org/download/releases/3.0/?) - Pyhton 3.6+ version
* [Selenium](https://github.com/SeleniumHQ/selenium) - Selenium for web automation
* [PyCharm](https://www.jetbrains.com/pycharm/) - IDE

## Installing 
**Python Installing**

* Download [Python 3](https://www.python.org/download/releases/3.0/?) from given the link.  
* And while you're installing make sure to check the box that says Add Python 3.x to PATH as shown to ensure that the interpreter will be placed in your execution path.

![ ](https://user-images.githubusercontent.com/22459679/53161894-e786ec80-35db-11e9-89ec-dbd807c9c3b0.PNG)

You can check your Python is correctly installed like below.

![ ](https://user-images.githubusercontent.com/22459679/53161895-e81f8300-35db-11e9-9b7e-753a292c6fe2.PNG)

Once you’ve confirmed that Python is correctly installed, you can proceed with installing Pip.
* Download [get-pip.py](https://bootstrap.pypa.io/get-pip.py) to a folder on your computer.
* Open a command prompt and navigate to the folder containing get-pip.py.
* Run the following command:
```
python get-pip.py
```
You can verify that pip was installed correctly by opening a command prompt and entering the following command:

![ ](https://user-images.githubusercontent.com/22459679/53163696-b7414d00-35df-11e9-9e18-61a90c0f311b.PNG)

**Selenium Installing**

* Install Selenium 
```sh
$ pip install selenium
```

* Selenium requires a driver to interface with the chosen browser.
 >  [Click for Chrome](https://sites.google.com/a/chromium.org/chromedriver/downloads)
 
 >  [Click for FireFox](https://github.com/mozilla/geckodriver/releases)
 
 >  [Click for safari](https://webkit.org/blog/6900/webdriver-support-in-safari-10)

* Extract the downloaded driver onto a folder.

* Test your setup

```
from selenium import webdriver
    import time
    driver= webdriver.Chrome()
    driver.get('http://google.com')
    time.sleep(2)
    driver.close()
```
**PyCharm Installing**

* Download [PyCharm](https://www.jetbrains.com/pycharm/)
* Run the PyCharm.exe file you've downloaded.
* Follow the instructions in the installation wizard.

## Methods


**get ()**
It is used to open specified url browser in windows.
```
//to launch the browser
driver.get(http://google.com);
```

**page_source()**
It is used to get the source of current load page
```
...
new_source = driver.page_source
print(new_source)
...
```
**close()**
Close the current window, if there are multiple windows, it will close the current window which is active.
```
driver.get(“http://www.google.com”);
driver.close();
```
**quit()**
It is used to close every associated window which is opened.
```
driver.get(“http://www.google.com”);
driver.quit();
```
**maximize_window()**
It is used to maximize new window.
```
driver.get(“http://www.google.com”);
driver.maximize_window()
```

**find_element_by..()**
It is used to find the first element using the given method.

* **find_element_by_id**

This is the most efficient and preferred method to locate an element. Id's are generally unique values.

![ ](https://user-images.githubusercontent.com/22459679/53169621-d8f60080-35ee-11e9-93d3-fae2f4b3a717.PNG)

```
driver.find_element_by_id("reset").click()
```

* **find_element_by_name**

Use this when you know name attribute of an element. 

![ ](https://user-images.githubusercontent.com/22459679/53169863-7fda9c80-35ef-11e9-973a-ef14349cf709.PNG)

```
element=driver.find_element_by_name("fmt")
```

* **find_element_by_class_name**

This is used by locating element by their class name.

![ ](https://user-images.githubusercontent.com/22459679/53170625-a13c8800-35f1-11e9-85b9-b9a03f3abb64.PNG)

```
driver.find_element_by_class_name("favorite styled")
```

* **find_element_by_xpath**

This is most popular and easiest way to locate elements.

![ ](https://user-images.githubusercontent.com/22459679/53171414-af8ba380-35f3-11e9-9025-9d3702e93a63.PNG)

```
driver.find_element_by_xpath('//input[@placeholder="Must be unique"]')
```

**find_elements_by..()**

It is used to find all elements within the current page

## Running the tests

* Open command prompt.
* Go to your project folder. 
``` 
cd C:\Users\your\project\location
``` 
* Run your test.py class.
``` 
python test.py
``` 
* Browser will open automatically and will close itself.

