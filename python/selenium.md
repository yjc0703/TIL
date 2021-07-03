# Selenium

> 웹 테스팅 자동화 도구. 동적 스크래핑에 사용.

### 크롬 드라이버
- 크롬 브라우저와 동일한 버전으로 다운로드
- https://chromedriver.chromium.org/downloads

### 설치
```
pip install selenium
```

### import
```python
from selenium import webdriver # 웹 드라이버
from selenium.webdriver.common.by import By # 엘리먼트 찾는 방법 설정
```

### open browser
```python
driver = webdriver.Chrome('웹 드라이버 설치경로')
driver.get('URL')
```

### usage
```python
# id 로 찾기
element = driver.find_element(By.ID, 'id')
element = driver.find_element_by_id('id')

# name으로 찾기
element = driver.find_element(By.NAME, 'name')
element = driver.find_element_by_name('name')

# class 로 찾기
element = driver.find_element(By.CLASS_NAME, 'class')
element = driver.find_element_by_class_name('class')

# selector 로 찾기
element = driver.find_element(By.CSS_SELECTOR, 'selector')
element = driver.find_element_by_css_selector('selector')

# tag 로 찾기
element = driver.find_element(By.TAG_NAME, 'tagName')
element = driver.find_element_by_tag_name('tagName')

# xpath 로 찾기
element = driver.find_element(By.XPATH, 'xpath')
element = driver.find_element_by_xpath('xpath')

# 키보드 입력
element.send_keys('keys')

# 클릭
element.click()
```


### 팝업 처리

```python
driver.switch_to.window(driver.window_handles[1]) # 새로생긴 첫번째 윈도우 팝업으로
driver.close()                                    # 팝업 닫기

driver.switch_to.window(driver.window_handles[0]) # 최초 윈도우로
```



### iframe 처리
``` python
driver.switch_to.frame('iframe') # iframe 선택
driver.switch_to.parent_frame()  # 부모 프레임 선택
```