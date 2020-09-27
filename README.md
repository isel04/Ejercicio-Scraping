# Ejercicio-Scraping

Scraping Vínculos
import urllib.request
datos = urllib.request.urlopen('https://peru21.pe/archivo/').read().decode()
import sys
!{sys.executable} -m pip install beautifulsoup4
from bs4 import BeautifulSoup
soup = BeautifulSoup(datos)
tags = soup('a')
for tag in tags:
    print(tag.get('href'))
