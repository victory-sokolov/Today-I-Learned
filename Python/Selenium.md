# Selenium


### Drag and drop element in Trello board

```python
def drag_card(self):
  # card number source counting from 0
	card = self.driver.find_elements(By.CLASS_NAME, "list-card-details") 
		
	# bord number target counting from 0
	content = self.driver.find_elements(By.CLASS_NAME, "js-list-content") 

	action = ActionChains(self.driver)
	action.drag_and_drop(card[0], content[1]).perform()
```
