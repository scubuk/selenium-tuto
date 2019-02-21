# Python Selenium Web Testing

## Prerequisites
* [Python 3+](https://www.python.org/download/releases/3.0/?) - Pyhton 3.6+ version
* [Selenium](https://github.com/SeleniumHQ/selenium) - Selenium for web automation
* [PyCharm](https://www.jetbrains.com/pycharm/)-IDE

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

## Deployment


1. get ().
It is used to open specified url browser in windows.
```
//to launch the browser
driver.get(http://google.com);
```

2. getPageSource().
It is used to get the source of current load page
```
//to launch the browser
driver.get(“http://www.google.com”);
pagesource=driver.getPageSource();
print(pagesource);
```
3. close().
Close the current window, if there are multiple windows, it will close the current window which is active.
```
driver.get(“http://www.google.com”);
driver.close();
```
4. quit().
It is used to close every associated window which is opened.
```
driver.get(“http://www.google.com”);
driver.quit();
```
5. findElement().
It is used to find the first WebElement using the given method.
```
//to launch the browser
driver.get(“http://www.gmail.com”);
WebElement gmaillink=driver.findElement(By.id());
System.out.println(gmaillink.getText());
```
6. findElements().
It is used to find all elements within the current page
```
//to launch the browser
driver.get(“http://www.facebook.com”);
//to findelements
List links=driver.findElements(By.TagName(“a”));
//Counting no of links in result page
System.out.println(links.size());
``` 
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

[Title] (link) 

<code>  Kod örnegi </code>

![İsim] (https://i.hizliresim.com/V0Jv7q.png)

![resim] (face1.png)
