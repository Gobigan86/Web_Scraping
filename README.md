# 🕸️ Scraping a Website using BeautifulSoup and Requests

This repository contains a simple Python script that uses the **BeautifulSoup** and **Requests** libraries to perform basic web scraping. The script is designed to connect to a target website and extract various elements from its HTML content.

---

## 📄 Table of Contents

* [Introduction](#introduction)
* [Installation](#installation)
* [Code Explanation](#code-explanation)

---

## ✨ Introduction

This script demonstrates the foundational steps for any web scraping project: making an HTTP request to fetch a page and then using a parsing library to navigate and extract data from the resulting HTML. Specifically, it extracts **tags**, the page **title**, **raw text**, and **links**.

---

## 🛠️ Installation

To run this script, you need to have the following Python packages installed. We recommend using `pip`:

pip install beautifulsoup4
pip install requests

* All tags: `tags = soup.find_all()`
* Title: `title = soup.find('title')`
* Text: `text = soup.get_text()`
* First anchor tag: `element = soup.find('a')`
* All anchor tags: `link = soup.find_all('a')`

## 💻 Code Explanation

Importing Libraries
CopyRun
from bs4 import BeautifulSoup
import requests
The script imports the BeautifulSoup class from the beautifulsoup4 library and the requests library to send HTTP requests.

Setting up the URL
CopyRun
url = 'https://www.scrapethissite.com/pages/forms/'
The script defines the URL of the website to be scraped.

Sending an HTTP Request
CopyRun
page = requests.get(url)
The script sends an HTTP GET request to the specified URL and stores the response in the page variable.

Parsing the HTML
CopyRun
soup = BeautifulSoup(page.text, 'html')
The script parses the HTML content of the response using the BeautifulSoup class.

Extracting Elements
The script extracts various elements from the parsed HTML, including:

All tags: tags = soup.find_all()
Title: title = soup.find('title')
Text: text = soup.get_text()
First anchor tag: element = soup.find('a')
All anchor tags: link = soup.find_all('a')




