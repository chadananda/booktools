## Book Processing Tools for Importing Librivox Books

### Initial Workflow:
  1. op: search
  2. op: listen (if necessary) & rate
  3. fetch (from Librivox & Gutenberg)  
  4. !! proofread & manual cleanup of HTML
  5. align
  6. proofread
  7. package (with notes)
  8. submit (by emailing package zip file)
  9. inflate (by our editors, fetches and prepares audio)
  10. !! audio post-processing (by audio engineer)
  10. import into library


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

