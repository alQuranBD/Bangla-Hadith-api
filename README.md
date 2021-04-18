# Bangla-Hadith-api

This is an REST API of a Huge Hadith collection of different hadith books contains Hadiths in Arabic, Bangla and English


**List of the Hadith books**
----
  Returns json data of all Hadith Books.

* **URL**

  **``http://alquranbd.com/api/hadith``**

* **Method:**
  `GET`
  
*  **URL Params:**
  `none`

* **Response Example:**

  * **Code:** 200 <br />
    **Content:** `{ id : 12, name : "Michael Bloom" }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "User doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/users/1",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```
