from io import BytesIO
from zipfile import ZipFile
from urllib.request import urlopen
from urllib.error import HTTPError
import openpyxl
url1='https://www.bseindia.com/download/BhavCopy/Equity/'
d=[str(x) for x in input('Enter the date of Equity Bhavcopy (date format=dd-mm-yy):- ').split('-')]
date=''.join(d)
Eq='EQ'
csv='_CSV.ZIP'
URL=url1+Eq+date+csv
print(URL)
try:
    with urlopen(URL) as zipresp:
            with ZipFile(BytesIO(zipresp.read())) as zfile:
                zfile.extractall()
            print('Equity file found successfully for the given date')

except HTTPError:
    print('"No file found for given date"')
