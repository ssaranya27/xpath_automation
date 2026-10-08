# xpath_automation

 Name: Saranya S
Website: https://www.tutorialspoint.com/selenium/practice/selenium_automation_practice.php
Date: 08/10/2026
# Automation Code:
```
import time
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait,Select
from selenium.webdriver.support import expected_conditions as EC


driver = webdriver.Edge()
wait=WebDriverWait(driver, 10)
driver.get("https://www.tutorialspoint.com/selenium/practice/selenium_automation_practice.php")
f_name=wait.until(EC.visibility_of_element_located((By.XPATH,'//input[@placeholder="First Name"]')))
f_name.send_keys("saranya")
email=wait.until(EC.visibility_of_element_located((By.XPATH,"//input[@id='email']")))
email.send_keys("ssaraya@gmail.com")

female = driver.find_element(
    By.XPATH,
    "//label[normalize-space()='Female']/preceding-sibling::input"
)
female.click()
mobile=wait.until(EC.visibility_of_element_located((By.XPATH,"//input[@placeholder='Enter Mobile Number']")))
mobile.send_keys("7010273445")
dob = wait.until(EC.visibility_of_element_located((By.CSS_SELECTOR, "input[type='date']")))
dob.send_keys("27-07-2005")
sub=wait.until(EC.visibility_of_element_located((By.XPATH,"//input[@id='subjects']")))
sub.send_keys("software development")
sports = wait.until(EC.element_to_be_clickable((By.XPATH, "//label[text()='Sports']/preceding-sibling::input")))
sports.click()
reading = wait.until(
    EC.element_to_be_clickable(
        (By.XPATH, "//label[text()='Reading']/preceding-sibling::input")
    )
)
picture=wait.until(EC.element_to_be_clickable((By.XPATH,"//input[@id='picture']")))
picture.send_keys(r"C:\Users\ssara\Downloads\ChatGPT Image May 21, 2026, 10_52_05 AM.png")
address=wait.until(EC.visibility_of_element_located((By.XPATH,"//textarea[@placeholder='Currend Address']")))
address.send_keys("13,kulakarai st")
address.send_keys("vellore")
address.send_keys("katpadi")
state=Select(wait.until(EC.element_to_be_clickable((By.XPATH,"//select[@name='state']"))))
state.select_by_visible_text("Uttar Pradesh")

city=Select(wait.until(EC.element_to_be_clickable((By.XPATH,"//select[@id='city']"))))
city.select_by_visible_text("Agra")

wait.until(
    EC.element_to_be_clickable(
        (By.CSS_SELECTOR, "input[type='submit'][value='Login']")
    )
).click()
time.sleep(5)

```
