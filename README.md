## WARNING
THIS TOOL IS NOT MEANT TO CIRCUMVENT COPYRIGHT PROTECTION. IT SHOULD ONLY BE USED TO DOWNLOAD ETEXTBOOKS THAT **YOU OWN**. REPRODUCING AND/OR DISTRIBUTING COPYRIGHTED WORK IS A CRIME IN MANY COUNTRIES AND JURISDICTIONS. 

# CheggDownloader
This is a simple Python script that allows you to download an eTextbook from Chegg.com.

## Requirements
1. Python 3
2. Google Chrome
3. `browser_cookie3`
4. `requests`
5. The eTextbook you are downloading must allow itself to be printed (limited pages OK)

## Usage
1. Make sure that you have purchased the eTextbook from Chegg (they have a generous 14-day return policy). 
2. **Using Chrome**, go to the eReader website (https://ereader.chegg.com) and log in.
3. Open the book you want to download. Record the e-ISBN number as shown in the URL. It should be the 13-digit number after `/books/`.
4. Click on the "Print" icon and record the maximum number of pages you are allowed to download at once (the larger the number, the faster the book can be downloaded).
5. Find the starting and ending page that you would like to download.
6. Start downloading
  ```bash
  $ pip install -r requirements.txt
  $ python3 CheggDownloader.py <paste e-ISBN here> <starting page> <ending page> -i <maximum pages you can download at once>
  $ # Example
  $ python3 CheggDownloader.py 1234567890123 1 999 -i 5
  ```
  
### Downloading unnumbered pages
If some pages in the book are unnumbered, or are not numbered with Arabic numerals (e.g. numbered with Roman numerals), you may use
```bash
$ python3 CheggDownloader.py <e-ISBN> -p <pages separated by space>
$ # Example
$ python3 CheggDownloader.py 1234567890123 -p i ii iii iv v
```

## Options
See the help message: `python3 CheggDownloader.py -h`
