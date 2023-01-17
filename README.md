# NO
no
from selenium import webdriver 
 
driver = webdriver.Chrome() 
driver.get('https://web.whatsapp.com/') 
 
input('Authenticate WhatsApp with QR code.') 
 
contact = input('Enter the name of contact: ') 
driver.find_element_by_xpath('//span[text()= contact]').click() 
 
n = int(input('Enter no of msgs.: ')) 
text = input('Enter text: ') 
 
for i in range(n): 
    driver.find_element_by_xpath('//*[@id="main"]/footer/div[1]/div[2]/div/div[1]/div/div[2]').send_keys(text, '\n') 
print(n, 'messages sent successfully to ', contact) 
