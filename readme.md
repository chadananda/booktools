## Book Processing Tools for Importing Librivox Books

### Workflow:
#### Admin Books selection
  1. we use `booktools -search` and `booktools -listen` to select booklist
  2. we send booklist to editor

#### Editor cleanup
  3. editor uses `booktools -fetch` to download book and audio
  4. manually proofreads and fixes HTML 
  4. uses `booktools -align` and `booktools proof` to verify alignment
  5. uses `booktools -package` to ZIP up books for submission

#### Audio processing and import
  8. admin uses `booktools -inflate` to prepare audio 
  10. !! audio post-processing (by audio engineer)
  11. admin uses `booktools -publish` to prepare book for publishing, including splitting audio files into AAC m4u
  10. developer imports book into library


### Command Line Tools

* booktools > search (title or author phrase)
  * returns list of books matching title or author with urls or ids

* booktools > listen (url, title, author or id)
  * fetches link to audio of first match and plays 30 seconds from 1:30 to 2:00    

* booktools > fetch (url, title, author or id)
  * downloads all books matching into their own folders
  * tries to reformat gutenberg text into Ocn HTML
  * merges audio to single m3u file
  * generates a workflow readme file
 
* booktools > align (title or id, requires API Key and URL for alignement service)
  * looks for a mster HTML file and creates new alignment file (warns if mastered file missing) 
  * looks for merged m3u file
  * sends to alignment service, provides progress feedback      

* booktools > proof (title or id)
  * opens book in browser with popcorn aligner  

* booktools > package (title or id)
  * ZIPs up critical files for submission

* booktools > inflate (filename)
  * Inflates packaged ZIP file, fetches 

* booktools > publish (bookname)
  * locates masterd WAV file and translates it into m4u, splitting into smaller files on space



