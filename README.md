# Bangla-Hadith-api

This is an REST API of a Huge Hadith collection of different hadith books contains Hadiths in Arabic, Bangla and English


**List of the Hadith books**
----
  Returns json data of all Hadith Books.

* **URL**

  **``http://alquranbd.com/api/hadith``**
  
  ***Example:*** <br/>
  ``http://alquranbd.com/api/hadith``

* **Method:**
  `GET`
  
*  **URL Params:**
  `none`

* **Response Example:**

  * **Code:** 200 <br />
  *  **Content:** 
      ```
      [
        {
          "id": "1",
          "nameEnglish": "Sahih Bukhari (IFA)",
          "nameBengali": "সহীহ বুখারী (ইফাঃ)",
          "lastUpdate": "2015-02-21",
          "isActive": "1",
          "priority": "2",
          "publisherId": "1",
          "section_number": "86",
          "hadith_number": "7053",
          "book_key": "bukhari"
        },
        {
          "id": "2",
          "nameEnglish": "Sahih Muslim (IFA)",
          "nameBengali": "সহীহ মুসলিম (ইফাঃ)",
          "lastUpdate": "2015-02-21",
          "isActive": "1",
          "priority": "3",
          "publisherId": "1",
          "section_number": "57",
          "hadith_number": "7283",
          "book_key": "muslim"
        },
        ...
        ...
        ...
      ```


**Chapters list of a book**
----
  Returns json data of all the chapters of a Hadith Book.

* **URL**

  **``https://alquranbd.com/api/hadith/:book_key``**
  
  ***Example:*** <br/>
  ``https://alquranbd.com/api/hadith/bukhari``

* **Method:**
  `GET`
  
*  **URL Params:**
  `book_key`

  | `book_key` 's value 	| Chapters of the book<br>(will return)                     	| Request url example                             	|
  |---------------------	|-----------------------------------------------------------	|-------------------------------------------------	|
  | `bukhari`             	| Sahih Bukhari (IFA)<br>সহীহ বুখারী (ইফাঃ)                  	| https://alquranbd.com/api/hadith/bukhari        	|
  | `muslim`              	| Sahih Muslim (IFA)<br>সহীহ মুসলিম (ইফাঃ)                   	| https://alquranbd.com/api/hadith/muslim         	|
  | `riyadusSalihin`      	| Riyajus Saolehin<br>রিয়াযুস স্বা-লিহীন                      	| https://alquranbd.com/api/hadith/riyadusSalihin 	|
  | `abuDaud`             	| Sunan Abu Daud (IFA)<br>সূনান আবু দাউদ (ইফাঃ)               	| https://alquranbd.com/api/hadith/abuDaud        	|
  | `ibnMajah`            	| Sunan'e Ibn Majah<br>সুনানে ইবনে মাজাহ                     	| https://alquranbd.com/api/hadith/ibnMajah       	|
  | `tirmidi`             	| Jami Tirmidi<br>সূনান তিরমিজী (ইফাঃ)                       	| https://alquranbd.com/api/hadith/tirmidi        	|
  |                     	| Sahih Bukhari (Tawhid)<br>সহীহ বুখারী (তাওহীদ)             	| upcoming                                        	|
  |                     	| Sahih Hadith'e Qudsi<br>সহিহ হাদিসে কুদসি                  	| upcoming                                        	|
  |                     	| 40 Hadith Nawawi<br>আন্‌-নওয়াবীর চল্লিশ হাদীস                	| upcoming                                        	|
  |                     	| Al-lulu<br>আল-লুলু ওয়াল মারজান                              	| upcoming                                        	|
  |                     	| Al-Adabul Mufrad<br>আল-আদাবুল মুফরাদ                        	| upcoming                                        	|
  |                     	| Sunan Ad-Daremi<br>সুনান আদ-দারেমী                         	| upcoming                                        	|
  | `muslimHA`            	| Sahih Muslim (Hadith Academy)<br>সহীহ মুসলিম (হাঃ একাডেমী) 	| https://alquranbd.com/api/hadith/muslimHA       	|
  |                     	| Sahih Shamayele Tirmidi<br>সহীহ শামায়েলে তিরমিযী          	| upcoming                                        	|


* **Response Example:**

  * **Code:** 200 <br />
  *  **Content:** 
      ```
      [
        {
          "nameEnglish": "Revelation",
          "nameBengali": "১/ ওহীর সূচনা",
          "lastUpdate": "2015-05-13",
          "isActive": "1",
          "id": "1",
          "chSerial": "1",
          "bookId": "1",
          "hadith_number": "6",
          "range_start": "1",
          "range_end": "6",
          "bookInitial": "bukhari"
        },
        {
          "nameEnglish": "Belief ",
          "nameBengali": "২/ ঈমান",
          "lastUpdate": "2015-05-13",
          "isActive": "1",
          "id": "4",
          "chSerial": "2",
          "bookId": "1",
          "hadith_number": "50",
          "range_start": "7",
          "range_end": "56",
          "bookInitial": "bukhari"
        },
        {
          "nameEnglish": "Knowledge",
          "nameBengali": "৩/ ইলম বা জ্ঞান",
          "lastUpdate": "2015-05-13",
          "isActive": "1",
          "id": "6",
          "chSerial": "3",
          "bookId": "1",
          "hadith_number": "80",
          "range_start": "57",
          "range_end": "136",
          "bookInitial": "bukhari"
        },        ...
        ...
        ...
      ```
