# Selenium
# selenium-java-testing

<p align="center"><a href="https://selenium.dev"><img src="https://selenium.dev/images/selenium_logo_square_green.png" width="100" alt="Selenium"/></a></p>

<p align="center" class="hero__title"><b>All-in-one Browser Automation Framework:<br />Web Crawling / Scraping / Testing / Reporting</b></p>

<p align="center"><a href="https://seleniumbase.io"><img src="https://img.shields.io/badge/docs-seleniumbase.io-11BBAA.svg" alt="SeleniumBase Docs"/></a></p>


Selenium is an umbrella project encapsulating a variety of tools and
libraries enabling web browser automation. Selenium specifically
provides an infrastructure for the [W3C WebDriver specification](https://w3c.github.io/webdriver/)
— a platform and language-neutral coding interface compatible with all
major web browsers.

Selenium's source code is made available under the [Apache 2.0 license](https://github.com/SeleniumHQ/selenium/blob/trunk/LICENSE).

[Selenium Server](https://www.selenium.dev/downloads/) supports two sets of commands simultaneously - for
new version [(WebDriver Google Chrome)](https://chromedriver.chromium.org/downloads) and old version [(Selenium RC)](https://www.selenium.dev/documentation/legacy/selenium_1/).


<b>
 <h2>What is Selenium?</h2>
</b>
<p>Due to the diverse focus
of the software, and confusion in terminology, many people mistake Selenium for a specific product for a single service. Selenium is a free (open source) automated testing environment
that is used to test web applications in
different browsers and on different platforms. We can use different programming languages, such as Java, to create Selenium test scripts, 
C#, Python, Ruby, PHP, etc
.
Selenium Software is not just a tool, but a software package (a set of tools),
each part of which meets different needs in the organization of testing. Here is a list of tools that are included in Selenium Software</p>
<ol>
  <li>Selenium WebDriver</li>
  <li>Selenium RC</li>
  <li>Selenium Grid</li>
</ol>

<h2>Why do We need to use Selenium?</h2>
<p>Selenium is now the standard for automating the execution of tests in browsers. Selenium is open source, no licensing costs are required, which is a great advantage
compared to other testing tools</p>
Advantages of using Selenium:
<ul>
  <li>Test scripts can be written in any of these programming languages: Java, Python, 
C #, PHP, Ruby, Perl</li>
  <li>Tests can be performed on any of these operating systems: Windows, Mac, or Linux.</li>
  <li>Tests can be performed in any browser: Mozilla 
Firefox, Internet Explorer, Google Chrome, Microsoft 
Edge, Safari or Opera.</li>
<li>Selenium can be integrated with tools such as TestNG and JUnit to manage test
cases and generate reports</li>
  <li>Selenium can be integrated with Maven, Jenkins and Docker to ensure continuous testing</li>
</ul>


## Contributing

Please read [CONTRIBUTING.md](https://github.com/SeleniumHQ/selenium/blob/trunk/CONTRIBUTING.md)
before submitting your pull requests.


## Installing

These are the requirements to create your own local dev environment to contribute to Selenium.

### All Platforms
* [Bazelisk](https://github.com/bazelbuild/bazelisk), a Bazel wrapper that automatically downloads
  the version of Bazel specified in `.bazelversion` file and transparently passes through all
  command-line arguments to the real Bazel binary.
* Java JDK version 17 or greater (e.g., [Java 17 Temurin](https://adoptium.net/temurin/releases/?version=17))
  * Set `JAVA_HOME` environment variable to location of Java executable (the JDK not the JRE)
  * To test this, try running the command `javac`. This command won't exist if you only have the JRE
  installed. If you're met with a list of command-line options, you're referencing the JDK properly.

### MacOS
  * Xcode including the command-line tools. Install the latest version using: `xcode-select --install`
  * Rosetta for Apple Silicon Macs. Add `build --host_platform=//:rosetta` to the `.bazelrc.local` file. We are working
  to make sure this isn't required in the long run.

### Windows
Several years ago [Jim Evans](https://www.linkedin.com/in/jimevansmusic/) published a great article on
[Setting Up a Windows Development Environment for the Selenium .NET Language Bindings](https://jimevansmusic.blogspot.com/2020/04/setting-up-windows-development.html);
This article is out of date, but it includes more detailed descriptions and screenshots that some people might find useful.

## Pre-requisites

Before you can start performing Java automation testing with Selenium, you would need to:

- Install the latest **Java development environment** i.e. **JDK 1.6** or higher. We recommend using the latest version.
- Download the latest **Selenium Client** and its **WebDriver bindings** from the [official website](https://www.selenium.dev/downloads/). Latest versions of Selenium Client and WebDriver are ideal for running your automation script on LambdaTest Selenium cloud grid.

- Install **Maven** which supports **JUnit** framework out of the box. **Maven** can be downloaded and installed following the steps from [the official website](https://maven.apache.org/).

#### Selenium Standalone

- Manual Installation - https://github.com/lmc-eu/steward/wiki/Selenium-server-&-browser-drivers
- Automated Installation - https://www.npmjs.com/package/selenium-standalone
- URL - http://localhost:4444/wd/hub

##### Installation and Launch
<ol>
 
 <li>Step I : Install IntelliJ IDEA</li>
<ul><li>https://www.jetbrains.com/idea/download/?ysclid=lu9zuetvnf195589274&section=windows</li></ul>
 <li>Step II : Install selenium-standalone.Latest stable version 3.141.59</li>
 <ul><li>https://tencrypto.github.io/downloads/</li></ul>

</ol>
<hr>
# In Windows, Run CMD as Administrator
<p>A new version of Java is installed, we check it via the Command line</p>

 ```
selenium-standalone start -- java -version
```
#### Selenium Grid
- URL -http://localhost:4444/grid/console

##### Installation and Launch
- Step III

```
selenium-standalone start -- -role hub
selenium-standalone start -- -role node -hub http://localhost:4444/grid/register
selenium-standalone start -- -role node -hub http://localhost:4444/grid/register -port 5556
```
```
selenium-standalone start -- -role node -hub http://localhost:4444/grid/register -browser browserName=Chrome
selenium-andalone start -- -role node -hub http://localhost:4444/grid/register -port 5556 -browser browserName=chrome,maxInstances=2
```
## 1. Installing JDK version 17
The `JDK` is a full-featured development kit. A set of software for `Java`, including `JRE`, compilers and tools (such as `JavaDoc` and `Java Debugger`), which exists for creating and compiling program. If you want, just run the `Java` program in your browser or computer, it will be enough for you installed `JRE`. But if you plan to program if you are using `Java`, you will also need the `JDK`.

* Download `Java Platform JDK 17` from the official website
    ```
    https://www.oracle.com/java/technologies/downloads/
    ```
* Install `java` with default settings
* Set the variable `“Java home”`
    * If the machine is `Windows`, press `Win+R` and type-those `sysdm.cpl` go to the advanced tab/Environment Variables.
    * Create a variable: `JAVA_HOME`.
    * Variable value: `<path where it is installed java>` for example `(C:\Program Files\Java\jdk*.*.*_**)`.
    * You also need to add the value: `<path whereupdated java>\bin`.
    * to the `PATH` variable: Click `Edit` and add: `C:\Program Files\Java\jdk*.*.*_**\bin`.
* After setting the variable you should restart `cmd console`. Let's check `java` in `cmd`:
    ```
    java –version
    ```
    ```
    javac –version
    ```
* If you see the `java` version in the `console`, then `java` is installed updated successfully.
## 2. Installing IntelliJ IDEA
* Download `IntelliJ IDEA` from the official website
    ```
    https://www.jetbrains.com/ru-ru/idea/
* Install `IntelliJ IDEA` with default settings
## 3. Loading the Selenium Java Client Driver
You can download `Selenium Java Client Driver` by going to link:
```
https://www.selenium.dev/downloads/
```
The page will contain a list of client `drivers` for other languages, but we select only the driver for `Java`.

This download comes as a `ZIP` file named
`"selenium-server-standalone-3.141.59.jar"`. For further simplicity, use
download, extract the contents of this `ZIP` file to a disk `C` so that you have a directory `"C:\selenium\"`.
## 4. Browser driver installation: Windows
Let's describe an example of installing a browser `driver
Chrome`. To install, open the website:

![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/main/src/chrome/chrome_24x24.png) Chrome
```bash
https://googlechromelabs.github.io/chrome-for-testing/
```
and download that `ChromeDriver` version that matches your `version` your `browser`.
To find out your `browser version`, open a new window in `Chrome`, in the search bar type:
```bash
chrome://version/
```
and press `Enter`. In the top line you will see information information about the `browser version`.

Unzip the downloaded file. Create on disk `C:` `webdrivers` folder and put the unzipped folder place the file `chromedriver.exe` in the `C:\webdrivers` folder.

Add the `C:\` folder to the system `PATH` variable `webdrivers`.
## 5. Selenium Server Standalone
Launch server performed one chosen in the command line (calling the `windows` `command line` is is done by typing the `cmd` command in the search):
```bash
cd ..
```
```bash
cd ..
```
* `Selenium Grid` — is a tool that works tests on multiple physical or virtual machines buses so scripts can be executed in parallel But. Essentially, [Selenium Grid]
* `Selenium Grid` — is a tool that works tests on multiple physical or virtual machines buses so scripts can be executed in parallel But. Essentially, [Selenium Grid](https://www.selenium.dev/documentation/grid/) is a cluster consisting of several `Selenium servers`. It is intended for organization of a distributed network, allowing parallel run multiple browsers simultaneously on a large network number of cars.
* `Hub` —  is a server that acts as a price the starting point where the tests will be run. [Selenium Grid](https://www.selenium.dev/documentation/grid/) has only one hub and starts runs on one machine once.
* `Node` — are `Selenium` instances that are attached captives to the concentrator, and which perform tests. There may be one or more nodes in the mesh, which These can be any `OS` and can contain any from supported `browsers`.
    * First we have to start the central server (hub). This is done using the following command:
      ```bash
      java -jar C:\selenium-server-standalone-3.141.59.jar -role hub
      ```
    * Before starting, make sure you are in the directory with the file `selenium-server-standalone.jar`.
    * In the console you should see information about successful start of hub.
      ```bash
      11:54:52.596 INFO - Nodes should register to
      http://192.168.99.1:4444/grid/register/
      11:54:52.596 INFO - Selenium Grid hub is up and running
      ```
    * After running the command, you can go to the hub administration panel at:
  ```bash
      http://localhost:4444/grid/
      ```
    * Open a new console window in which we enter the following command:
      ```bash
      java -Dwebdriver.chrome.driver="C:\chromedriver\chromedriver.exe" -jar C:\selenium-server-standalone-3.141.59.jar -role node -hub http://192.168.99.1:4444/grid/register/
      ```
    * Check the current state of our selenium hub, and also see which nodes are ready to work and which browsers are available in them, you can go to the browser line to the address where selenium hub is running. In our case it is `http://192.168.99.1:4444/` and from there we go to the selenium grid hub console. In the console we see that there is currently one node connected to the hub. When node starts, it can't determine which browsers are available and therefore use a standard configuration consisting of `5 chrome browsers`, `5 firefox` and `1 IE`.

#  1. Selenium + Java
## 1.1 Connect Selenium to IntelliJ project

Go to 

    https://www.selenium.dev/downloads/
Find `Java` among the available languages and click on `Download`

![image](https://github.com/ArtemA1ekseev/selenium-java-testing/assets/113195869/efe013f2-f986-4f4b-9816-c0a448fe56fb)

Unpack the `archive`. The content will be something like this:

![image](https://github.com/ArtemA1ekseev/selenium-java-testing/assets/113195869/d7aa20b8-87cf-4fe1-bb61-0faa51f76d25)

Open your project in `IntelliJ` and click `File → Project Structure`
Select `Modules`, then click on the plus on the right and select `1. JARs or directories…`

![image](https://github.com/ArtemA1ekseev/selenium-java-testing/assets/113195869/d96b75ce-e6f3-41a3-a1f1-afd549d21a39)

Go to the folder where you just extracted the archive and select all the `.jar` files from the root and from the `libs` subfolder

Click `OK`
![image](https://github.com/ArtemA1ekseev/selenium-java-testing/assets/113195869/749ba53c-a49f-45ee-9510-29876a37c937)

## 1.2 Connect browser driver

No matter what `programming language` you write the `code` in, the operation of connecting the `browser driver` is approximately the same.

You can read about this in the article [Connecting the browser driver in Selenium](https://testsetup.ru/selenium/#driver)

## 1.3 Simple test

To make sure `Selenium` is connected successfully, paste the following code and compile it.

```java
package org.test;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class WebDriverDemo1 {
    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("https://www.selenium.dev/selenium/web/web-form.html"); //opens the browser and navigates to the URL
        

    }
}
```
If you do not want or cannot edit the `PATH` variable, try registering the path to the driver - insert before the line `WebDriver driver = ...`

```java
driver.get("https://www.selenium.dev/selenium/web/web-form.html"); //opens the browser and navigates to the URL
```

#  2. Search for elements
## 2.1 Simple test

First of all, you need to connect `By` in `Java`, this is done as follows:

```java
import org.openqa.selenium.By;
```

Often it is not enough to simply find an element. To perform some actions on what you find, connect `WebElement`

```java
import org.openqa.selenium.WebElement;
```

## 2.2 Filling out a simple form
Let's use the most reliable method - by `id`. After examining the source code of the page you will see the following code

```html
<input type="text" id="name1" name="url1">
```

Therefore, the required id is `name1`

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverDemo2 {

    public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver


        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement searchField =
                driver.findElement(By.id("name1"));

        searchField.sendKeys("topbicycle.ru");
        searchField.submit();
    }
```
## 2.3 Click on the link - search by text

Using `linkText`, find all links with the text `Renovation`, select the first one and click on it.

```java
package org.test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverDemo3 {

    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement renovationLink =
                driver.findElements(By.linkText("Renovation")).get(0);
        renovationLink.click();
    }
}
```
## 2.4 Click on the link - search by CSS selector

All links in this example also have the same text - `Italy`. But we can't use the same technique, so let's study the page code and find out that the desired link has a `march8` class

We will look for a link, that is, cssSelector `a`, with the `march8` class

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverDemo4 {

    public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement march8Link =
                driver.findElements(By.cssSelector("a[class=march8]")).get(0);
        march8Link.click();
    }
}
```
## 2.5 Click on the image

Now let's look at the picture. Let's use the tag search.

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverDemo5 {

    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver
WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement imageLink =
                driver.findElements(By.tagName("img")).get(1); 
        imageLink.click();
    }
}
```
#  3. Switches

You need to find it on the page www.urn.su/IT/selenium/basic_test/ switch and put it in the `Lannister` position
As a check, output the contents to the `terminal`.

I used the `list`, so I imported the `import java.util.List`;

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

import java.util.List;

public class WebDriverDemo6 {
    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver
WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        List<WebElement> radioButtons =
                driver.findElements(By.name("house"));
        radioButtons.get(1).click();

        for (WebElement radioButton : radioButtons) {

            if (radioButton.isSelected()) {
                System.out.println(radioButton.getAttribute("value"));
            }
        }
    }
}
```
#  4. Checkboxes
You need to find it on the page www.urn.su/ui/basic_test/ `checkboxes` and mark `Cersei`

After studying the page code, you can understand that the desired element has an `id`, so it is very easy to find it.

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverDemo7 {

    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver
driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement checkbox =
                driver.findElement(By.id("cerseiId"));
        checkbox.click();
    }
}
```

#  5. Drop-down lists

You need to find it on the page www.urn.su/ui/basic_test/ checkboxes and select `Dawn`

I will use `Select`, so I need to pre-connect `import org.openqa.selenium.support.ui.Select`;

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class WebDriverDemo8 {

    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement selectElement =
                driver.findElement(By.id("swords"));
        Select select = new Select(selectElement);
        select.selectByVisibleText("Dawn");
    }
}
```
#  6. Tables

You need to find it on the page www.urn.su/ui/basic_test/ table. An internal table is nested in the external table. You need to get to the element in the third row of the nested table. To check, we will output the contents of this element to the terminal.

Pay attention to lines 14, 15 and 16. First, the driver finds the external table, then I no longer call driver, but search only in the external table, and then only in the internal table.

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebDriverDemo9 {

    public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver

        WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        driver.get("http://www.urn.su/ui/basic_test/"); //opens the browser and navigates to the URL

        WebElement outerTable =
                driver.findElement(By.tagName("table"));
        WebElement innerTable =
                outerTable.findElement(By.tagName("table"));
        WebElement row =
                innerTable.findElements(By.tagName("td")).get(2);
        System.out.println(row.getText());
    }
}
```
#  7. Wait for the element to appear
The elements can be loaded onto the page at different speeds. To save yourself from unnecessary headaches, you need to make the most of Selenium's capabilities

In the following example, you can visit the site search page `urn.su` wait for the `Yandex` script to load, insert the word java into the search, just to be safe, wait for the Find button to load and `click` on it.

```java
package org.test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.WebDriverWait;
import static org.openqa.selenium.support.ui.ExpectedConditions.presenceOfElementLocated;

public class WebDriverDemo10 {

    public static void main(String[] args) {

        System.setProperty("webdriver.chrome.driver", "C:\\chromedriver\\chromedriver.exe"); //setting the path for chrome driver
WebDriver driver = new ChromeDriver(); //creating object for chrome driver

        // explicit wait
        WebDriverWait wait = new WebDriverWait(driver, 50);

        driver.get("http://www.urn.su/search.php"); //opens the browser and navigates to the URL

        try {
            WebElement yandexField =
                    wait.until(presenceOfElementLocated(By.name("text")));
            yandexField.sendKeys("java");
        }
        catch (Exception e) {
            e.printStackTrace();
        }

        try {
            WebElement yButton =
                    wait.until(presenceOfElementLocated(By.className("ya-site-form__submit")));
            yButton.click();
  }

        catch (Exception e) {
            e.printStackTrace();
        }

    }
}
```
#  7.1 Implicit expectation

The timeout set using Implicit Wait is a global setting for `WebDriver`. Every time you need to find an item on a page, `WebDriver` will search either until it finds it or until that time has passed.

Every `500 ms`, WebDriver will access the `DOM` for the presence of the desired element.
#  7.2 Explicit Wait

Explicit waiting in `Selenium` is used to tell the `web driver` to wait for certain conditions `(Expected Conditions)` or exceed the maximum time before throwing an `“ElementNotVisibleException"` exception. This is an intelligent kind of `expectation`, but it can only be applied to the specified elements. This provides better features than implicit expectation, as it waits for dynamically loaded `Ajax` elements.

Once we declare an explicit expectation, we have to use `“ExpectedConditions” `or we can configure how often we want to check the condition using Fluent Wait. Nowadays, we use Thread for `implementation.Sleep()` is generally not recommended to use.


#### Code Snippets

##### Maven Dependencies

###### Junit
```xml
  <dependencies>
  
    <dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-java</artifactId>
      <version>3.13.0</version>
      <scope>test</scope>
    </dependency>

  
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.12</version>
      <scope>test</scope>
    </dependency>
  
  </dependencies>
```
###### Test NG

```xml
<dependencies>

    <dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-java</artifactId>
      <version>3.13.0</version>
      <scope>test</scope>
    </dependency>


    <dependency>
      <groupId>org.testng</groupId>
      <artifactId>testng</artifactId>
      <version>6.14.3</version>
      <scope>test</scope>
    </dependency>

  </dependencies>


```

###### Other Dependencies

```xml

    <dependency>
      <groupId>org.apache.poi</groupId>
      <artifactId>poi</artifactId>
      <version>3.6</version>
      <scope>test</scope>
    </dependency>

    <dependency>
      <groupId>org.apache.poi</groupId>

<artifactId>poi-ooxml</artifactId>
      <version>3.6</version>
      <scope>test</scope>
    </dependency>

```
###### Test Selenium Dependencies(Example)
```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>org.testing</groupId>
    <artifactId>selenium-java-test</artifactId>
    <version>1.0-SNAPSHOT</version>


    <dependencies>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>4.17.0</version>
        </dependency>

        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-server</artifactId>
            <version>3.141.59</version>
        </dependency>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
<version>RELEASE</version>
            <scope>compile</scope>
        </dependency>
    </dependencies>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

</project>
```


###### Chrome Driver/Java Code

```
  ChromeDriverManager.getInstance().setup();
  driver = new ChromeDriver();
```

###### Firefox Driver/Java Code

```
  FirefoxDriverManager.getInstance().setup();
  driver = new FirefoxDriver();
```

######  Test Selenium
```
package org.testing;


import org.junit.Test;
import org.openqa.selenium.Platform;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.remote.DesiredCapabilities;
import org.openqa.selenium.remote.RemoteWebDriver;

import java.net.MalformedURLException;
import java.net.URL;

/**
 * Web page testing class.
*
 * @version 1.0.0
 * @autor Nat167 (Nataliya Likhacheva)
 */
public class Test1 {

    /*
       ______     __
      / ____/__  / /__  ____  (_)_  ______ ___
      \__ \/ _ \/ / _ \/ __ \/ / / / / __ `__ \
    ___/ /  __/ /  __/ / / / / /_/ / / / / / /
    /____/\___/_/\___/_/ /_/_/\__,_/_/ /_/ /_/
    ------------------------------------------

    */

    /**
     * The method opens the page and checks its title in the browser.
     *
     * @throws MalformedURLException
     */
    @Test
    public void test1() throws MalformedURLException {

        DesiredCapabilities capability = new DesiredCapabilities();
        capability.setBrowserName("chrome");
        capability.setPlatform(Platform.WIN10);
        // Create a new driver instance.
        WebDriver driver;
        driver = new RemoteWebDriver(new URL("http://192.168.99.1:4444/wd/hub"), capability);
        driver.manage().window().maximize();
        // Opening a page in the browser.
        driver.get("https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstley");
        // Check the page title.
System.out.println("Title of the page is " + driver.getTitle());
        // After the test you need to close the browser.
        driver.quit();

    }
}
```

   - File -> Import -> Existing Maven Project -> Navigate to the folder where you unzipped the zip
   - Select the right project
- Choose the Spring Boot Application file (search for file with @SpringBootApplication)
- Right Click on the file and Run as Java Application
- You are all Set


