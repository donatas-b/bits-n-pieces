## Initialize  

// NuGet: Selenium.WebDriver.ChromeDriver 

```
using OpenQA.Selenium.Chrome;  
IWebDriver driver = new ChromeDriver();
```  

// NuGet: Selenium.Mozilla.Firefox.Webdriver  
```
using OpenQA.Selenium.Firefox;
IWebDriver driver = new FirefoxDriver();
```

// NuGet: Selenium.WebDriver.IEDriver  
```
using OpenQA.Selenium.IE;
IWebDriver driver = new InternetExplorerDriver();
```

// NuGet: Selenium.WebDriver.EdgeDriver  
```
using OpenQA.Selenium.Edge;
IWebDriver driver = new EdgeDriver();
```

## Basic Browser Operations
// Navigate to a page  
```
this.driver.Navigate().GoToUrl(@"http://google.com");
```

// Get the title of the page  
```
string title = this.driver.Title;
```

// Get the current URL  
```
string url = this.driver.Url;
```

// Get the current page HTML source  
```
string html = this.driver.PageSource;
```

## Close

//close only the current window on which Selenium is running automated tests. The WebDriver session, however, remains active
```
IWebDriver driver=new ChromeDriver();
driver.close();
```

//close all browser windows and ends the WebDriver session
```
IWebDriver driver=new ChromeDriver();
driver.quit();
```

## Locators - FindElement

//single element  
```
this.driver.FindElement(By.ClassName("className"));
this.driver.FindElement(By.CssSelector("css"));
this.driver.FindElement(By.Id("id"));
this.driver.FindElement(By.LinkText("text"));
this.driver.FindElement(By.Name("name"));
this.driver.FindElement(By.PartialLinkText("pText"));
this.driver.FindElement(By.TagName("input"));
this.driver.FindElement(By.XPath("//*[@id='editor']"));
```

// Find multiple elements  
```
IReadOnlyCollection<IWebElement> anchors = this.driver.FindElements(By.TagName("a"));
```

// Search for an element inside another  
```
var div = this.driver.FindElement(By.TagName("div")).FindElement(By.TagName("a"));
```

// elements in POM class
```
public IWebElement BtnHome => webDriver.FindElement(By.TagName("button"));
```

## Locators - FindsBy 
```
[FindsBy(How = How.Id, Using = "userName")]
[FindsBy(How = How.ClassName, Using = "panel other")]
[FindsBy(How = How.CssSelector, Using = "#userName")]
[FindsBy(How = How.LinkText, Using = "Automate The Planet")]
[FindsBy(How = How.Name, Using = "webDriverCheatSheet")]
[FindsBy(How = How.PartialLinkText, Using = "Automate")]
[FindsBy(How = How.TagName, Using = "a")]
[FindsBy(How = How.XPath, Using = "//*[@id='panel']/div/h1")]
private IWebElement _myElement;
```

## Basic Elements Operations  
```
IWebElement element = driver.FindElement(By.Id("id"));
element.Click();
element.SendKeys("someText");
element.Clear();
element.Submit();
string innerText = element.Text;
bool isEnabled = element.Enabled;
bool isDisplayed = element.Displayed;
bool isSelected = element.Selected;
```

```
SelectElement select = new SelectElement(element);
select.SelectByIndex(1);
select.SelectByText("Ford");
select.SelectByValue("ford");
select.DeselectAll();
select.DeselectByIndex(1);
select.DeselectByText("Ford");
select.DeselectByValue("ford");
```

```
IWebElement selectedOption = select.SelectedOption;
IList<IWebElement> allSelected = select.AllSelectedOptions;
bool isMultipleSelect = select.IsMultiple;
```

## Advanced Element Operations
// Drag and Drop
```
IWebElement element = driver.FindElement(By.XPath("//*[@id='project']/p[1]/div/div[2]"));
Actions move = new Actions(driver);
move.DragAndDropToOffset(element, 30, 0).Perform();
```

// How to check if an element is visible
```
Assert.IsTrue(driver.FindElement(By.XPath("//*[@id='tve_editor']/div")).Displayed);
```

// Upload a file
```
IWebElement element = driver.FindElement(By.Id("RadUpload1file0"));
String filePath = @"D:\WebDriver.Series.Tests\\WebDriver.xml";
element.SendKeys(filePath);
```

// Scroll focus to control
```
IWebElement link = driver.FindElement(By.PartialLinkText("Previous post"));
string js = string.Format("window.scroll(0, {0});", link.Location.Y);
((IJavaScriptExecutor)driver).ExecuteScript(js);
link.Click();
```

// Focus on a control
```
IWebElement link = driver.FindElement(By.PartialLinkText("Previous post"));
```


## Waits

//**Implicit** - global setting that applies to every element location call for the entire session. The default value is 0
```
IWebDriver driver = new ChromeDriver();
driver.Manage().Timeouts().ImplicitWait = TimeSpan.FromSeconds(5);
```

// **Explicit** - loops added to the code that poll (every 250 ms) the application for a specific condition to evaluate as true before it exits the loop and continues to the next command in the code. Selenium Wait class automatically waits for the designated element to exist.
```
WebDriverWait wait = new WebDriverWait(driver, TimeSpan.FromSeconds(30));
wait.Until(ExpectedConditions.VisibilityOfAllElementsLocatedBy(By.XPath("//*[@id='tve_editor']/div[2]/div[2]/div/div")));
```

### Expected Coditions
```
alertIsPresent()
elementSelectionStateToBe()
elementToBeClickable()
elementToBeSelected()
frameToBeAvaliableAndSwitchToIt()
invisibilityOfTheElementLocated()
invisibilityOfElementWithText()
presenceOfAllElementsLocatedBy()
presenceOfElementLocated()
textToBePresentInElement()
textToBePresentInElementLocated()
textToBePresentInElementValue()
titleIs()
titleContains()
visibilityOf()
visibilityOfAllElements()
visibilityOfAllElementsLocatedBy()
visibilityOfElementLocated()
```

//**Fluent** - major difference between *fluent* wait and *explicit* wait is that the polling frequency at which the presence for the web element is checked is controllable in *fluent* wait
```
DefaultWait<IWebDriver> fluentWait = new DefaultWait<IWebDriver>(driver);
fluentWait.Timeout = TimeSpan.FromSeconds(5);
fluentWait.PollingInterval = TimeSpan.FromMilliseconds(250);
// Ignore the exception - NoSuchElementException that indicates that the element is not present
fluentWait.IgnoreExceptionTypes(typeof(NoSuchElementException));
fluentWait.Message = "Element to be searched not found";
```

## Advanced Browser Operations
// Handle JavaScript pop-ups
```
IAlert a = driver.SwitchTo().Alert();
a.Accept();
a.Dismiss();
//send value to the alert box
a.SendKeys("tests");
//getting the text present inside the alert box
var alerttext=a.Text;
```

// Switch to frames
```
this.driver.SwitchTo().Frame(1);
this.driver.SwitchTo().Frame("frameName");
IWebElement element = this.driver.FindElement(By.Id("id"));
this.driver.SwitchTo().Frame(element);
```

// Switch to the default document (selects either the first frame on the web page or the main document)
```
this.driver.SwitchTo().DefaultContent();
```

// Switch between browser windows or tabs
```
ReadOnlyCollection<string> windowHandles = driver.WindowHandles;
string firstTab = windowHandles.First();
string lastTab = windowHandles.Last();
driver.SwitchTo().Window(lastTab);
```

// Navigation history
```
this.driver.Navigate().Back();
this.driver.Navigate().Refresh();
this.driver.Navigate().Forward();
```

// Maximize window
```
this.driver.Manage().Window.Maximize();
```

// Wait until a page is fully loaded via JavaScript
```
WebDriverWait wait = new WebDriverWait(this.driver,
TimeSpan.FromSeconds(30));
wait.Until((x) =>
{return ((IJavaScriptExecutor)this.driver).ExecuteScript("return document.readyState").Equals("complete");});
```

## Cookies

// Add a new cookie
```
Cookie cookie = new OpenQA.Selenium.Cookie("key", "value");
this.driver.Manage().Cookies.AddCookie(cookie);
```

// Get all cookies
```
var cookies = this.driver.Manage().Cookies.AllCookies;
```

// Delete a cookie by name
```
this.driver.Manage().Cookies.DeleteCookieNamed("CookieName");
```

// Delete all cookies
```
this.driver.Manage().Cookies.DeleteAllCookies();
```


## Screenshots

// Taking an element screenshot
```
IWebElement element = driver.FindElement(By.XPath("//*[@id='tve_editor']/div"));
var cropArea = new Rectangle(element.Location, element.Size);
var bitmap = bmpScreen.Clone(cropArea, bmpScreen.PixelFormat);
bitmap.Save(fileName);
```

// Taking a full-screen screenshot
```
Screenshot screenshot = ((ITakesScreenshot)driver).GetScreenshot();
screenshot.SaveAsFile(@"pathToImage", ImageFormat.Png);
```

### Advanced Browser Confgurations

// Set a HTTP proxy Chrome
```
ChromeOptions options = new ChromeOptions();
var proxy = new Proxy();
proxy.Kind = ProxyKind.Manual;
proxy.IsAutoDetect = false;
proxy.HttpProxy = "127.0.0.1:3239";
proxy.SslProxy = "127.0.0.1:3239";
options.Proxy = proxy;
options.AddArgument("ignore-certificate-errors");
IWebDriver driver = new ChromeDriver(options);
```

// Accept all certificates Chrome
```
DesiredCapabilities capability = DesiredCapabilities.Chrome();
Environment.SetEnvironmentVariable("webdriver.chrome.driver", "C:\\PathToChromeDriver.exe");
capability.SetCapability(CapabilityType.AcceptSslCertificates, true);
IWebDriver driver = new RemoteWebDriver(capability);
```

// Set Chrome options.
```
ChromeOptions options = new ChromeOptions();
DesiredCapabilities dc = DesiredCapabilities.Chrome();
dc.SetCapability(ChromeOptions.Capability, options);
IWebDriver driver = new RemoteWebDriver(dc);
```

// Start Chrome with an unpacked extension
```
ChromeOptions options = new ChromeOptions();
options.AddArguments("load-extension=/pathTo/extension");
DesiredCapabilities capabilities = new DesiredCapabilities();
capabilities.SetCapability(ChromeOptions.Capability, options);
DesiredCapabilities dc = DesiredCapabilities.Chrome();
dc.SetCapability(ChromeOptions.Capability, options);
IWebDriver driver = new RemoteWebDriver(dc);
```

// Start Chrome with a packed extension
```
ChromeOptions options = new ChromeOptions();
options.AddExtension(Path.GetFullPath("localpathto/extension.crx"));
DesiredCapabilities capabilities = new DesiredCapabilities();
capabilities.SetCapability(ChromeOptions.Capability, options);
DesiredCapabilities dc = DesiredCapabilities.Chrome();
dc.SetCapability(ChromeOptions.Capability, options);
IWebDriver driver = new RemoteWebDriver(dc);
```


## ??

// Option 1.
link.SendKeys(string.Empty);
// Option 2.
((IJavaScriptExecutor)driver).ExecuteScript("arguments[0].focus();",
link);





