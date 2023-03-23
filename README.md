# Java-selenium
java selenium code
package UI;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;


public class Login {
	public static void main (String[]args) throws InterruptedException {
		
		ChromeOptions co = new ChromeOptions();
		co.addArguments("--remote-allow-origins=*");
		WebDriver driver = new ChromeDriver(co);
		//driver.get("https://www.orangehrm.com/");
		System.out.println(driver.getTitle());
		driver.get("https://www.ebay.com/");
		driver.manage().window().maximize();
		Thread.sleep(2000);
		driver.findElement(By.xpath("//*[@id=\"gh-ac\"]")).sendKeys("moblie");
		driver.findElement(By.xpath("//*[@id=\\\"gh-btn\\\"]")).click();
		driver.close();
		driver.quit();
	}

}

