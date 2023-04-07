package org.example;

import io.github.bonigarcia.wdm.WebDriverManager;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.edge.EdgeDriver;
import org.openqa.selenium.safari.SafariDriver;
import org.testng.annotations.*;

public class githubTesting
{
    WebDriver driver;

    @BeforeClass
    @Parameters( {"browser","url"})
    void setupDriver(String browser, String link){

        if(browser.equalsIgnoreCase("chrome"))
        {
            WebDriverManager.chromedriver().setup();
            driver = new ChromeDriver();
        }
        else if(browser.equalsIgnoreCase("edge"))
        {
            WebDriverManager.edgedriver().setup();
            driver = new EdgeDriver();
        }
        driver.get(link);
        driver.manage().window().maximize(); //Full screen.
    }



    @Test
    void getTitleFromHomePage() throws InterruptedException
    {
        driver.findElement(By.xpath("/html/body/div[1]/div[1]/header/div/div[2]/div/div/div[2]/a")).click();
        Thread.sleep(1000);

        driver.findElement(By.cssSelector("input#login_field")).sendKeys("bikashsharma1");
        Thread.sleep(1000);
        driver.findElement(By.cssSelector("input#password")).sendKeys("Bikash@@02082000");
        Thread.sleep(3000);
        driver.findElement(By.cssSelector("input[value='Sign in']")).click();
        Thread.sleep(3000);
    }
    @AfterClass
    void closeDriver()
    {
        driver.close();
    }
}
