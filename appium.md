Install node.js and npm

npm install -g appium
npm install -g appium-doctor (java only)



appium driver install windows

...

i Driver windows@2.12.24 successfully installed
- automationName: Windows
- platformNames: ["Windows"]

https://blogs.windows.com/windowsdeveloper/2018/06/20/introducing-winappdriver-ui-recorder/

dotnet add package Microsoft.WinAppDriver.Appium.WebDriver --version 1.0.1-Preview

dotnet add package Appium.WebDriver
dotnet add package Newtonsoft.Json --version 13.0.3


shell:appsfolder

new solution
add nuget Appium.WebDriver 4.4.5

            AppiumOptions options = new AppiumOptions();
            options.AddAdditionalCapability("app", "Microsoft.WindowsCalculator_8wekyb3d8bbwe!App");
            options.AddAdditionalCapability("app", "Microsoft.ZuneVideo_8wekyb3d8bbwe!Microsoft.ZuneVideo");

            WindowsDriver<WindowsElement> session = new WindowsDriver<WindowsElement>(new Uri(@"http://127.0.0.1:4723"), options);

            session.Manage().Timeouts().ImplicitWait = TimeSpan.FromSeconds(2);

            session.FindElementByAccessibilityId("AutomationId");
            session.FindElementByClassName("");
            session.FindElementByCssSelector("");
            session.FindElementById("");
            session.FindElementByImage("");
            session.FindElementByLinkText("");
            session.FindElementByName("Name");
            session.FindElementByPartialLinkText("");
            session.FindElementByTagName("");
            session.FindElementByWindowsUIAutomation("");
            session.FindElementByXPath("");

            var selectAll = session.FindElementByName("Copy");
            WebDriverWait wait = new WebDriverWait(session, TimeSpan.FromSeconds(5));
            wait.Until(a => selectAll.Displayed);

            selectAll.GetAttribute("Name);


            var result = session.FindElementByAccessibilityId("CalculatorResults");
            result.SendKeys("12347");
            Actions action = new Actions(session);
            action.MoveToElement(result);
            action.MoveToElement(result, offsetX, offsetY);
            action.ContextClick(result);
            action.Perform();


            List<ActionSequence> actionSequencesList = new List<ActionSequence>();
            PointerInputDevice touchContact = new PointerInputDevice(PointerKind.Touch);
            ActionSequence touchSequence = new ActionSequence(touchContact, 0);
            touchSequence.AddAction(touchContact.CreatePointerMove(inkCanvas, -radius, -radius, TimeSpan.Zero));
            .....
            session.PerformActions(actionSequencesList);




Microsoft.WindowsCalculator_8wekyb3d8bbwe!App


"c:\Program Files (x86)\Windows Application Driver\WinAppDriver.exe" 21000

"C:\Program Files\nodejs\node.exe" "C:\Users\donatas\AppData\Roaming\npm\node_modules\appium\build\lib\main.js" --port "4723" --address "127.0.0.1"



OpenQA.Selenium.Appium.Service.Exceptions.AppiumServerHasNotBeenStartedLocallyException: 'The local appium server has not been started. The given Node.js executable: C:\Program Files\nodejs\node.exe Arguments: "C:\Users\donatas\AppData\Roaming\npm\node_modules\appium\build\lib\main.js" --port "4723" --address "127.0.0.1". 
Time 120000 ms for the service starting has been expired!'


OpenQA.Selenium.Appium.Service.Exceptions.AppiumServerHasNotBeenStartedLocallyException: 'The local appium server has not been started. The given Node.js executable: C:\Program Files\nodejs\node.exe Arguments: "C:\Users\donatas\AppData\Roaming\npm\node_modules\appium\build\lib\main.js" --port "4723" --address "127.0.0.1". 
Time 120000 ms for the service starting has been expired!'



Toggle navigation
Alarm
Add an alarm