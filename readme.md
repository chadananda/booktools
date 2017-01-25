## Book Processing Tools for IRLS

### Desired Workflow:
  1. search
  2. listen (if necessary) & rate
  3. fetch (from librivox) or import (from Ocean)
  4. !! manual cleanup and mastering
  5. align
  6. proof


### Command Line Tools

* booktools > search (title or author phrase)
  * returns list of books matching title or author with urls or ids


* booktools > listen (url, title, author or id)
  * fetches link to audio of first match and plays 30 seconds from 1:30 to 2:00
      

* booktools > fetch (url, title, author or id)
  * downloads all books matching into their own folders
  * tries to reformat gutenberg text into Ocn HTML
  * converts audio to 16bit WAV and merges into a single file
  * generates a workflow readme file
      
      
* booktools > import (url)
  * downloads document in txt or Ocn and reformats as necessry 
  * tries to locate audio, converts to 16bit WAV and merges into a single file
  * generates a workflow readme file
 
 
* booktools > align (title or id)
  * looks for a masterd WAVE file and generates m4u from WAV file (warns if missing)
  * looks for a mster HTML file and creates new alignment file (warns if mastered file missing)  
      
      
* booktools > proof (title or id)
  * opens book in browser with popcorn aligner  