# selenium-projects

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

public class loadtime {
	
	

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		WebDriver driver;
		System.setProperty("webdriver.chrome.driver","C:\\selenium\\chromedriver_win32\\chromedriver.exe");
		driver = new ChromeDriver();
		long startTime = System.currentTimeMillis();

		driver.get("http://www.bml.edu.in/");

		new WebDriverWait(driver, 10).until(ExpectedConditions.presenceOfElementLocated(By.id("page")));

		long endTime = System.currentTimeMillis();

		long totalTime = endTime - startTime;

		System.out.println("Total Page Load Time: " + totalTime + "milliseconds");
	}

}
