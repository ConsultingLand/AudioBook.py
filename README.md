# AudioBook.py
Create audiobook by few Python line of code

import pyttsx3
import PyPDF2
book = open('oopy.pdf', 'rb')
pdfReader = PyPDF2.PdfFileReader(book)
pages = pdfReader.numPages
print(pages)
speaker = pyttsx3.init()

page = pdfReader.getPage(7)
text = page.extractText()
speaker.say(text)
speaker.say('iam getting happier and happier')
speaker.runAndWait()
