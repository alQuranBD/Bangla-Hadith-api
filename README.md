# Bangla-Hadith-api

This is an REST API of a huge Hadith collection of different hadith books contain Hadiths in Arabic, Bangla and English

<p align="left"> <img src="https://komarev.com/ghpvc/?username=niamulhasan&label=Profile%20views&color=0e75b6&style=flat" alt="niamulhasan" /> </p>


# The API at a glance

 **ROOT URI : ``http://alquranbd.com/api/``**


| URI                                                  | Parameters                                                                 | Response                                       | Example Call                                                         |
|------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------|----------------------------------------------------------------------|
| ROOT/hadith                                          | none                                                                       | JSON List of the Hadith books                  | <sub><sup>http://alquranbd.com/api/hadith<sub><sup>                  |
| ROOT/hadith/`:book_key`                              | `book_key` : String (Check the values in "Chapters list of a book" table)  | JSON Chapters list of a book                   | <sub><sup>https://alquranbd.com/api/hadith/bukhari<sub><sup>         |
| ROOT/hadith/`:book_key`/`:chapter_no`                | `book_key` : String <br/> `chapter_no` : Integer                           | JSON list of all Hadiths from a Chapter        | <sub><sup>https://alquranbd.com/api/hadith/bukhari/1<sub><sup>       |
| ROOT/api/hadith/`:book_key`/`:chapter_no`/`:page_no` | `book_key` : String <br/> `chapter_no` : Integer <br/> `page_no` : Integer | JSON Hadiths from a Chapter devided into Pages | <sub><sup>https://alquranbd.com/api/hadith/bukhari/2/2<sub><sup>     |
| ROOT/hadith/`:book_key`/`:chapter_no`/pages          | `book_key` : String <br/> `chapter_no` : Integer                           | JSON Page Numbers from a Chapter               | <sub><sup>https://alquranbd.com/api/hadith/bukhari/2/pages<sub><sup> |





# Details


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
        ...
        ...
        ...
      ```




**Get all Hadiths from a Chapter**
----
  Returns json data of all the Hadiths of a chapter from a Hadith Book.

* **URL**

  **``https://alquranbd.com/api/hadith/:book_key/:chapter_no``**
  
  ***Example:*** <br/>
  ``https://alquranbd.com/api/hadith/bukhari/1``

* **Method:**
  `GET`
  
*  **URL Params:**
  `book_key`
  `chapter_no`
  
  | Parameters   	| value type 	| Value Range                                                                        	|
  |--------------	|------------	|------------------------------------------------------------------------------------	|
  | `book_key`   	| String     	| Keys are listed in `Chapters list of a book` section                               	|
  | `chapter_no` 	| Integer    	| [1, x ]                                                                           	|

    x = ``count the response result from ``https://alquranbd.com/api/hadith/:book_key`` 

* **Response Example:**

  * **Code:** 200 <br />
  *  **Content:** 
      ```
      [
       {
          "hadithEnglish":"Narrated Umar bin Al-Khattab: I heard Allahs Messenger (sallallahu alaihi wa sallam) saying, The reward of deeds depends upon the intentions and every person will get the reward according to what he has intended. So whoever emigrated for worldly benefits or for a woman to marry, his emigration was for what he emigrated for.",
          "hadithArabic":"حَدَّثَنَا الْحُمَيْدِيُّ عَبْدُ اللَّهِ بْنُ الزُّبَيْرِ، قَالَ حَدَّثَنَا سُفْيَانُ، قَالَ حَدَّثَنَا يَحْيَى بْنُ سَعِيدٍ الأَنْصَارِيُّ، قَالَ أَخْبَرَنِي مُحَمَّدُ بْنُ إِبْرَاهِيمَ التَّيْمِيُّ، أَنَّهُ سَمِعَ عَلْقَمَةَ بْنَ وَقَّاصٍ اللَّيْثِيَّ، يَقُولُ سَمِعْتُ عُمَرَ بْنَ الْخَطَّابِ ـ رضى الله عنه ـ عَلَى الْمِنْبَرِ قَالَ سَمِعْتُ رَسُولَ اللَّهِ صلى الله عليه وسلم يَقُولُ إِنَّمَا الأَعْمَالُ بِالنِّيَّاتِ، وَإِنَّمَا لِكُلِّ امْرِئٍ مَا نَوَى، فَمَنْ كَانَتْ هِجْرَتُهُ إِلَى دُنْيَا يُصِيبُهَا أَوْ إِلَى امْرَأَةٍ يَنْكِحُهَا فَهِجْرَتُهُ إِلَى مَا هَاجَرَ إِلَيْهِ .",
          "hadithBengali":"১। হুমায়দী (রহঃ) আলকামা ইবনু ওয়াক্কাস আল-লায়সী (রহঃ) থেকে বর্ণিত, আমি উমর ইবনুল খাত্তাব (রাঃ)-কে মিম্বরের ওপর দাঁড়িয়ে বলতে শুনেছিঃ আমি রাসুলুল্লাহ সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম কে বলতে শুনেছিঃ প্রত্যেক কাজ নিয়তের সাথে সম্পর্কিত। আর মানুষ তার নিয়ত অনুযায়ী ফল পাবে। তাই যার হিজরত হবে দুনিয়া লাভের অথবা নারীকে বিয়ে করার উদ্দেশ্যে- সেই উদ্দেশ্যেই হবে তার হিজরতের প্রাপ্য।\n",
          "checkStatus":"1",
          "hadithNo":"1",
          "id":"1",
          "thesequence":"1",
          "isActive":"1",
          "chapterId":"1",
          "bookId":"1",
          "publisherId":"1",
          "sectionId":"1",
          "statusId":"1",
          "topicName":"১\/ রাসুলুল্লাহ সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম এর প্রতি কিভাবে ওহী শুরু হয়েছিল",
          "rabiNameBn":"উমর ইবনুল খাত্তাব (রাঃ)",
          "rabiNameEn":"Umar Ibnul Khattab (RA)"
       },
       {
          "hadithEnglish":"Narrated Aisha: (the mother of the faithful believers) Al-Harith bin Hisham asked Allahs Messenger (sallallahu alaihi wa sallam) O Allahs Messenger (sallallahu alaihi wa sallam)! How is the Divine Inspiration revealed to you? Allahs Messenger (sallallahu alaihi wa sallam) replied, Sometimes it is (revealed) like the ringing of a bell, this form of Inspiration is the hardest of all and then this state passes off after I have grasped what is inspired. Sometimes the Angel comes in the form of a man and talks to me and I grasp whatever he says. Aisha added: Verily I saw the Prophet (sallallahu alaihi wa sallam) being inspired divinely on a very cold day and noticed the sweat dropping from his forehead (as the Inspiration was over).",
          "hadithArabic":"حَدَّثَنَا عَبْدُ اللَّهِ بْنُ يُوسُفَ، قَالَ أَخْبَرَنَا مَالِكٌ، عَنْ هِشَامِ بْنِ عُرْوَةَ، عَنْ أَبِيهِ، عَنْ عَائِشَةَ أُمِّ الْمُؤْمِنِينَ ـ رضى الله عنها ـ أَنَّ الْحَارِثَ بْنَ هِشَامٍ ـ رضى الله عنه ـ سَأَلَ رَسُولَ اللَّهِ صلى الله عليه وسلم فَقَالَ يَا رَسُولَ اللَّهِ كَيْفَ يَأْتِيكَ الْوَحْىُ فَقَالَ رَسُولُ اللَّهِ صلى الله عليه وسلم أَحْيَانًا يَأْتِينِي مِثْلَ صَلْصَلَةِ الْجَرَسِ ـ وَهُوَ أَشَدُّهُ عَلَىَّ ـ فَيُفْصَمُ عَنِّي وَقَدْ وَعَيْتُ عَنْهُ مَا قَالَ، وَأَحْيَانًا يَتَمَثَّلُ لِيَ الْمَلَكُ رَجُلاً فَيُكَلِّمُنِي فَأَعِي مَا يَقُولُ . قَالَتْ عَائِشَةُ رضى الله عنها وَلَقَدْ رَأَيْتُهُ يَنْزِلُ عَلَيْهِ الْوَحْىُ فِي الْيَوْمِ الشَّدِيدِ الْبَرْدِ، فَيَفْصِمُ عَنْهُ وَإِنَّ جَبِينَهُ لَيَتَفَصَّدُ عَرَقًا.",
          "hadithBengali":"২। আবদুল্লাহ ইবনু ইউসুফ (রহঃ) আয়িশা (রাঃ) থেকে বর্ণিত, হারিস ইবনু হিশাম (রাঃ) রাসুলুল্লাহ সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম -কে জিজ্ঞাসা করলেন, ইয়া রাসুলুল্লাহ! আপনার প্রতি ওহী কিভাবে আসে? রাসুলুল্লাহ সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম বললেনঃ কোন সময় তা ঘন্টাধ্বনির ন্যায় আমার নিকট আসে। আর এটি-ই আমার উপর সবচাইতে কষ্টদায়ক হয় এবং তা সমাপ্ত হতেই ফিরিশতা যা বলেন আমি তা মুখস্থ করে নই, আবার কখনো ফিরিশতা মানুষের আকৃতিতে আমার সঙ্গে কথা বলেন। তিনি যা বলেন আমি তা মুখস্থ করে ফেলি। আয়িশা (রাঃ) বলেন, আমি প্রচন্ড শীতের দিনে ওহী নাযিলরত অবস্থায় তাঁকে দেখেছি। ওহী শেষ হলেই তাঁর কপাল থেকে ঘাম ঝরে পড়ত।\n",
          "checkStatus":"1",
          "hadithNo":"2",
          "id":"2",
          "thesequence":"2",
          "isActive":"1",
          "chapterId":"1",
          "bookId":"1",
          "publisherId":"1",
          "sectionId":"1",
          "statusId":"1",
          "topicName":"১\/ রাসুলুল্লাহ সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম এর প্রতি কিভাবে ওহী শুরু হয়েছিল",
          "rabiNameBn":"আয়িশা (রাঃ)",
          "rabiNameEn":"Ayesha (RA)"
       },        
        ...
        ...
        ...
      ```




**Get Hadiths from a Chapter in Pages**
----
  Returns json data of Hadiths devided into pages of a chapter from a Hadith Book.
  Each page contains 20 Hadiths.

* **URL**

  **``https://alquranbd.com/api/hadith/:book_key/:chapter_no/:page_no``**
  
  ***Example:*** <br/>
  ``https://alquranbd.com/api/hadith/bukhari/2/2``

* **Method:**
  `GET`
  
*  **URL Params:**
  `book_key`
  `chapter_no`
  `page_no`

  | Parameters   	| value type 	| Value Range                                          	|
  |--------------	|------------	|------------------------------------------------------	|
  | `book_key`   	| String     	| Keys are listed in `Chapters list of a book` section 	|
  | `chapter_no` 	| Integer    	| [1, x]                                               	|
  | `page_no`    	| Integer    	| [1, last_page]                                       	|


* **Response Example:**

  * **Code:** 200 <br />
  *  **Content:** 
      ```
         [
           {
              "hadithEnglish":"Narrated Abdullah bin Amr: A person asked Allahs Messenger (sallallahu alaihi wa sallam) . What (sort of) deeds in or (what qualities of) Islam are good? He replied, To feed (the poor) and greet those whom you know and those whom you dont know.",
              "hadithArabic":"حَدَّثَنَا قُتَيْبَةُ، قَالَ حَدَّثَنَا اللَّيْثُ، عَنْ يَزِيدَ بْنِ أَبِي حَبِيبٍ، عَنْ أَبِي الْخَيْرِ، عَنْ عَبْدِ اللَّهِ بْنِ عَمْرٍو، أَنَّ رَجُلاً، سَأَلَ رَسُولَ اللَّهِ صلى الله عليه وسلم أَىُّ الإِسْلاَمِ خَيْرٌ قَالَ تُطْعِمُ الطَّعَامَ، وَتَقْرَأُ السَّلاَمَ عَلَى مَنْ عَرَفْتَ وَمَنْ لَمْ تَعْرِفْ .",
              "hadithBengali":"২৭। কুতায়বা (রহঃ) আবদুল্লাহ ইবনু আমর (রাঃ) থেকে বর্ণিত, এক ব্যাক্তি রাসূল সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম কে জিজ্ঞাসা করল, ইসলামের কোন্ কাজ সবচাইতে উত্তম? তিনি বললেনঃ তুমি লোকদের আহার করাবে এবং পরিচিত-অপরিচিত নির্বিশেষে সকলকে সালাম দিবে।\n",
              "checkStatus":"1",
              "hadithNo":"27",
              "id":"30",
              "thesequence":"453",
              "isActive":"1",
              "chapterId":"20",
              "bookId":"1",
              "publisherId":"1",
              "sectionId":"4",
              "statusId":"1",
              "topicName":"২০\/ সালামের প্রচলন করা ইসলামের অন্তর্ভুক্ত",
              "rabiNameBn":"আবদুল্লাহ ইবনু আমর (রাঃ)",
              "rabiNameEn":"Abdullah Ibnu Amar (RA)"
           },
           {
              "hadithEnglish":"Narrated Ibn Abbas: The Prophet (sallallahu alaihi wa sallam) said: I was shown the Hell-fire and that the majority of its dwellers were women who were ungrateful. It was asked, Do they disbelieve in Allah? (or are they ungrateful to Allah?) He replied, They are ungrateful to their husbands and are ungrateful for the favors and the good (charitable deeds) done to them. If you have always been good (benevolent) to one of them and then she sees something in you (not of her liking), she will say, I have never received any good from you.",
              "hadithArabic":"حَدَّثَنَا عَبْدُ اللَّهِ بْنُ مَسْلَمَةَ، عَنْ مَالِكٍ، عَنْ زَيْدِ بْنِ أَسْلَمَ، عَنْ عَطَاءِ بْنِ يَسَارٍ، عَنِ ابْنِ عَبَّاسٍ، قَالَ قَالَ النَّبِيُّ صلى الله عليه وسلم أُرِيتُ النَّارَ فَإِذَا أَكْثَرُ أَهْلِهَا النِّسَاءُ يَكْفُرْنَ . قِيلَ أَيَكْفُرْنَ بِاللَّهِ قَالَ يَكْفُرْنَ الْعَشِيرَ، وَيَكْفُرْنَ الإِحْسَانَ، لَوْ أَحْسَنْتَ إِلَى إِحْدَاهُنَّ الدَّهْرَ ثُمَّ رَأَتْ مِنْكَ شَيْئًا قَالَتْ مَا رَأَيْتُ مِنْكَ خَيْرًا قَطُّ .",
              "hadithBengali":"২৮। আবদুল্লাহ ইবনু মাসলামা (রহঃ) ইবনু আব্বাস (রাঃ) থেকে বর্ণিত, তিনি বলেন, রাসূল সাল্লাল্লাহু আলাইহি ওয়াসাল্লাম ইরশাদ করেনঃ আমাকে জাহান্নাম দেখানো হয়। (আমি দেখি), তার অধিবাসীদের অধিকাংশই স্ত্রীলোক; (কারন) তারা কুফরী করে। জিজ্ঞাসা করা হল, তারা কি আল্লাহর সঙ্গে কুফরী করে? তিনি বললেনঃ তারা স্বামীর অবাধ্য হয় এবং ইহসান অস্বীকার করে। তুমি যদি দীর্ঘকাল তাদের কারো প্রতি ইহসান করতে থাক, এরপর সে তোমার সামান্য অবহেলা দেখলেই বলে, আমি কখনো তোমার কাছ থেকে ভালো ব্যবহার পাইনি। \n",
              "checkStatus":"1",
              "hadithNo":"28",
              "id":"31",
              "thesequence":"454",
              "isActive":"1",
              "chapterId":"21",
              "bookId":"1",
              "publisherId":"1",
              "sectionId":"4",
              "statusId":"1",
              "topicName":"২১\/ স্বামীর প্রতি অকৃতজ্ঞতা ",
              "rabiNameBn":"ইবনু আব্বাস (রাঃ)",
              "rabiNameEn":"Ibnu Abbas (RA)"
           }, 
        ...
        ...
        ...
      ```



**Get Page Numbers from a Chapter**
----
  Returns json data of Page Numbers of a chapter from a Hadith Book.
  We need the numbers of pages to show the Pagination List or Link. This api gives you the page numbers.
  Note: Each page contains 20 Hadiths.

* **URL**

  **``https://alquranbd.com/api/hadith/:book_key/:chapter_no/pages``**
  
  ***Example:*** <br/>
  ``https://alquranbd.com/api/hadith/bukhari/2/pages``

* **Method:**
  `GET`
  
*  **URL Params:**
  `book_key`
  `chapter_no`
  
| Parameters   	| value type 	| Value Range                                          	|
|--------------	|------------	|------------------------------------------------------	|
| `book_key`   	| String     	| Keys are listed in `Chapters list of a book` section 	|
| `chapter_no` 	| Integer    	| [1, x]                                               	|


* **Response Example:**

  * **Code:** 200 <br />
  *  **Content:** 
      ```
      [
        {
          "pageNo": 0
        },
        {
          "pageNo": 1
        },
        {
          "pageNo": 2
        },
        {
          "pageNo": 3
        }
      ]
      ```
