# Python Selenium Web Testing

## Prerequisites
* Python 3+ - Pyhton 3.6+ version
* Selenium - Selenium for web automation
* PyCharm - IDE

## Installing 
**Python Installing**

* Download [Python 3](https://www.python.org/download/releases/3.0/?) from given the link.
   
   ![ ](https://user-images.githubusercontent.com/22459679/53389876-2df49680-39a2-11e9-8e04-fad1a4b946df.PNG)
* And while you're installing make sure to check the box that says Add Python 3.x to PATH.

  ![ ](https://user-images.githubusercontent.com/22459679/53161894-e786ec80-35db-11e9-89ec-dbd807c9c3b0.PNG)

You can check your Python is correctly installed like below.

![ ](https://user-images.githubusercontent.com/22459679/53161895-e81f8300-35db-11e9-9b7e-753a292c6fe2.PNG)

Once you’ve confirmed that Python is correctly installed, you can proceed with installing Pip.
* Download [get-pip.py](https://bootstrap.pypa.io/get-pip.py) to a folder on your computer. Open the link and Right-Click | Save As.
* Run the file, it will update PIP.
* Open your cmd. (Windows+R and write cmd.)
* Navigate to the folder(using cd command)containing get-pip.py. 

   ![ ](https://user-images.githubusercontent.com/22459679/53339475-85015980-3917-11e9-8b8e-928805f0c33e.PNG)
* Run the following command:
```
> python get-pip.py
```
You can verify that pip was installed correctly by opening a command prompt and entering the following command:

![ ](https://user-images.githubusercontent.com/22459679/53163696-b7414d00-35df-11e9-9e18-61a90c0f311b.PNG)

**Selenium Installing**

Selenium is a browser automation tool. Portable framework for testing web application.

* Open your cmd and install Selenium. 
```sh
> pip install selenium
#OR
> pip install -U selenium
```
The optional –U will upgrade the existing version of the installed package to the latest version.

**Note:** If the following error occurred; 

![ ](https://user-images.githubusercontent.com/22459679/56344539-56408a80-61c6-11e9-8607-4752f9b8172a.png)

Change the proxy setting with run these commands;
```
set HTTP_PROXY=http://YOUR_ID:YOUR_PASSWORD@proxyuk.huawei.com:8080
set HTTPS_PROXY=http://YOUR_ID:YOUR_PASSWORD@proxyuk.huawei.com:8080
```

Verify that the installation was successfull.
```
pip show selenium
```

* Selenium requires a driver to interface with the chosen browser. Download one of them. 
 >  [Click for Chrome](http://chromedriver.chromium.org/downloads)
 
 >  [Click for FireFox](https://github.com/mozilla/geckodriver/releases)
 
 >  [Click for Safari](https://webkit.org/blog/6900/webdriver-support-in-safari-10)

* Extract the downloaded driver onto a folder.
* Keep your driver path. You'll need this.
* You are done.

**PyCharm Installing**

* Download [PyCharm](https://www.jetbrains.com/pycharm/) from this link.

   ![ ](https://user-images.githubusercontent.com/22459679/53341189-f5aa7500-391b-11e9-9bca-217954dc37a7.PNG)
   
* Run the PyCharm.exe file you've downloaded.
* Follow the instructions in the installation wizard.

## Creating a PyCharm Project

* Open PyCharm.
* Click Create New Project on the Welcome Screen.

<img src="https://www.jetbrains.com/help/img/idea/2018.3/py_welcomeScreen.png" width="700" height="500">

* Or on the main menu click File | New Project | Pure Python | Choose your project location.

* Click Create.

 ![ ](https://user-images.githubusercontent.com/22459679/53338074-cb54b980-3913-11e9-8339-2b01038e907a.png)
 
 ![ ](https://user-images.githubusercontent.com/22459679/53338136-ff2fdf00-3913-11e9-9bf7-5cc549aeb8ae.PNG)
 
* Create your Python Package to right click on your project name. New | Python Package.

![ ](https://user-images.githubusercontent.com/22459679/53338368-88dfac80-3914-11e9-9041-27f9e98459d1.png)

* Create your Python File by doing following steps.

![ ](https://user-images.githubusercontent.com/22459679/53338688-600be700-3915-11e9-868d-6014b4f2aef6.png)

* Write your Python file name like below and then click OK.

![ ](https://user-images.githubusercontent.com/22459679/53338918-f213ef80-3915-11e9-9189-ea7643b32c5e.PNG)

* Now, you are all set up for writing your test automation.

## Imported Library


``
from selenium import webdriver
import time
``

Selenium :

-It is using for using the automation.
-Control the webdriver.
–Perform actions like click(), refresh(), navigate to website..

Time:

-It is using for sleep function.(driver.sleep(10))
-Selenium works only when the all the elements of the page is loaded other ways it would be fail.


## Selenium Methods

When we get the driver object, with these methods that we can perform on a driver. Before we write these methods we have to import webdriver and test our setup(For running instructions go to 'Running the tests'). 

**Note:** You should specify your driver path. Example: driver= webdriver.Chrome("web/driver/path/chromedriver.exe")

```
from selenium import webdriver
    
    driver= webdriver.Chrome("your/web/driver/path")
    driver.get('http://google.com')
   
    driver.close()
```


**get ()**

It is used to open specified url browser in windows.
```
...
//to launch the browser
driver.get(http://google.com);
...
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
...
driver.get(“http://www.google.com”);
driver.close();
...
```

**quit()**

It is used to close every associated window which is opened.
```
...
driver.get(“http://www.google.com”);
driver.quit();
...
```

**maximize_window()**

It is used to maximize new window.
```
...
driver.get(“http://www.google.com”);
driver.maximize_window()
...
```

**back()**

This method does the same operation as clicking on the Back Button of any browser.
```
...
driver.back()
...
```

**time()**

It always force the browser to wait for a specific time. We need to import time class. Its not preferred method.
**import time**
```
...
driver.sleep(1000)
...
```
**set_page_load_timeout()**

Its used to set page loading time. 

```
...
driver.set_page_load_timeout(20)
...
```
**implicitly_wait()**

It is used to wait certain time before processing next following code.
```
...
driver.implicitly_wait(20)
...
```
**get_screenshot_as_file()**

It is used to get a screenshot of current page and save this as a specified file(png,jpeg..).
```
...
driver.get_screenshot_as_file("app3.png")
...
```

**switch_the_window()**

This is used to switching 2 open windows. Sometimes you open new window and you still in previous window. You need to switch between 2 windows.

```
...
driver.switch_to.window(driver.window_handles[-1])
driver.switch_to.window(driver.window_handles[0])
...
```

**find_element_by..()**

It is used to find the first element using the given method. 

* To learn web page element, Right Click on web page | Click Inspect.
 
  ![ ](https://user-images.githubusercontent.com/22459679/53395453-f2ae9380-39b2-11e9-8e1d-6d204faf0f8a.png)

* Click that item. 

  ![ ](https://user-images.githubusercontent.com/22459679/53395630-5df86580-39b3-11e9-918c-bc391d88e035.png)

* Select an element on the page to inspect it.

  ![ ](https://user-images.githubusercontent.com/22459679/53396024-7a48d200-39b4-11e9-8f3f-d7c83a8a85ad.png)

Now you can inspect your web element.


* **find_element_by_id**

This is the most efficient and preferred method to locate an element. Id's are generally unique values.

![ ](https://user-images.githubusercontent.com/22459679/53169621-d8f60080-35ee-11e9-93d3-fae2f4b3a717.PNG)

```
...
driver.find_element_by_id("reset")
...
```

* **find_element_by_name**

Use this when you know name attribute of an element. 

![ ](https://user-images.githubusercontent.com/22459679/53169863-7fda9c80-35ef-11e9-973a-ef14349cf709.PNG)

```
...
element=driver.find_element_by_name("fmt")
...
```

* **find_element_by_class_name**

This is used by locating element by their class name.

![ ](https://user-images.githubusercontent.com/22459679/53170625-a13c8800-35f1-11e9-85b9-b9a03f3abb64.PNG)

```
...
driver.find_element_by_class_name("favorite styled")
...
```

* **find_element_by_xpath**

In Selenium automation, if the elements are not found by the general locators like id, class, name then XPath is used to find an element on the web page.

XPath is defined as XML Path.

To find the xpath of html code; right click on the element, click copy and choose "Copy XPath".

![ ](https://user-images.githubusercontent.com/22459679/53171414-af8ba380-35f3-11e9-9025-9d3702e93a63.PNG)

**Types of XPath**

* Absolute Path

It is the direct way to find the element.
But disadvantage is that if there are any changes made in the path of the element then that Xpath gets failed. 

``
html/body/div[1]/section/div[1]/div/div/div/div[1]/div/div/div/div/div[3]/div[1]/div/h4[1]/b
``

* Relative Path

It starts with the double forward slash (//), which means it can search the element anywhere at the webpage.
You can start from the middle of the HTML structure and no need to write long xpath.

Xpath=//tagname[@attribute='value']

Below is the example of a relative XPath expression of the same element shown in the absolute path.

``
//*[@class='featured-box']//*[text()='Testing']
``

These are different usage of find_element_by_xpath;

```
...
driver.find_element_by_xpath('//input[@placeholder="Must be unique"]')
...
```
```
...
driver.find_element_by_xpath('//*[@id="user-edit-page"]/form/div[6]/div/div/input')
...
```
This is a [great tutorial for understanding the XPath] : (https://www.guru99.com/xpath-selenium.html)

**find_elements_by..()**

It is used to find all elements within the current page


## Selenium Operations and Elements

**click()**

This is used to click on web elements like link, button, radio button, checkbox, images.

```
...
driver.find_element_by_id("submitBtn").click()
...
```

**send_keys()**

This is used to sending inputs into text fields and text areas.

```
...
driver.find_element_by_xpath('//input[@placeholder="Enter role name or code"]').send_keys("test")
...
```

* You need to **import from selenium.webdriver.common.keys import Keys** to use keyboard keys(ENTER,CTRL..) as a key.

```
...
driver.find_element_by_xpath('//input[@placeholder="Enter role name or code"]').send_keys(Keys.ENTER)
...
```


## Running the tests from Cmd

* Open command prompt.
* Go to your project folder. 
``` 
cd C:\Users\your\project\location
``` 
* Run your test.py class.
``` 
python test.py
``` 
 ![ ](https://user-images.githubusercontent.com/22459679/53393390-4ae29700-39ad-11e9-80b9-2009c88185fb.PNG)
 
* Browser will open automatically and will close itself.

## Running the tests from PyCharm

* Use Ctrl + Shift + F10 shortcut.

* Or right click somewhere on your editor body and Click Run 'testAutomation.py'
* Or click green run button on main menu.

 ![ ](https://user-images.githubusercontent.com/22459679/53341326-4cb04a00-391c-11e9-963b-1a42d6699969.PNG)

* Browser will open automatically and will close itself.

