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
