# ThePenMan
<ins><b>Update : August 04 2021</b></ins><br>
<b> 1. Introduction</b> <br>
   This is the repository of my Semester 05 project "The Pen Man". 
   <p align="center">
   <img src="https://github.com/soujanyalohanathen/ThePenMan/blob/main/Imgs/plotter%20writing.jpg" width="auto">
   </p>
   <br>
<b> 2. Abstract of the problem </b> <br>
   Mostly many documents are accepted as printed materials now. But still there is a need of handwritten documents at some points. In these cases differently abled people specially people who are visually impaired or who have issues with mobility will face difficulties in writing the documents.
   
   Currently Existing Solutions : 
         1. For the Visully impaired People : Braille Writing Equipment or An assistance of another people.
         2. For people have mobility issues : An assistance of another people.
   In Sri Lanka, Having a assistant people to perform the writing tasks is the most common solution such as in Genereal Certified Exams. 
   <br>
   <br>
<b> 3. Solution</b> <br>
   The solution is to replace the assistant person with an automated xy plotter which can recognizes the user's voice and write the words told by the user.
   This is basically to combine the existing speech to text converter and the xy plotter using a programmed microcontroller.
   <br>
   <br>
<b> 4. Basically How a XY plotter Works? </b> <br>
    Once you feed the sketch into the XY Plotter's software It will scan out the sketch and according to the X and Y coordinates it will draw the exact image on to a paper.
    

https://user-images.githubusercontent.com/58034992/128229800-1e0f9ed3-e7cf-4f72-b51d-bfbc25fa789d.mp4
   <br>
   <br>
<b> 5. Planned Final Demonstration </b><br>
   The final demonstration will be on,<br>
      1. MakeBlock XY Plotter<br>
      <img src= "https://user-images.githubusercontent.com/58034992/128227932-94d287c1-3b14-4a62-872f-641c2f23bcd8.jpg" width="350">
      <br>
      2. Arduino UNO <br>
      <img src= "https://user-images.githubusercontent.com/58034992/128227993-021dda2f-d6cd-4598-bfc0-c87ddfbfccac.png" width="350">
      <br>
      3. ESP8266 Module <br>
      <img src= "https://user-images.githubusercontent.com/58034992/128228070-4cf643de-2d89-43e5-a1d3-f611c8d91df2.jpg" width ="350">
<br>
<br>
 <b> 6. Input Format </b><br>
   Input voice is set to be sent as the realtime voice as in Google Speech Recognizing System. 
   The sketches of the letters and numbers will be uploaded to the software.
   Already it has been tried to insert the audio file as .wav format as in the AudioSegmentType.py file. 
   It normally have the whole audio and cut it into segments called 'Audio Chunks' and recognizes them.
   The code given above is using 'pydub' library from Python.
   It has been noticed there were errors. And also this solution will be more applicable if the work can be done in real time.<br>![audiosegmenttype](https://user-           images.githubusercontent.com/58034992/129144509-84422496-f1d3-4e44-b928-284888b13b30.jpg) <br>


<ins><b>Update : August 12 2021</b></ins><br>
      
   Therefore it has been decided to create a mobile application with the assistance of Google Speech Recognition. 
   So far, the speech recognition app has a basic UI and it will be improved in coming weeks.<br>
   ![SpeechToTextImg](https://user-images.githubusercontent.com/58034992/129144927-e58a0d93-9946-405a-ae19-4e8aca7401f2.jpg) <br>
   
   Here is a demo of how it works !! <br>
   https://user-images.githubusercontent.com/58034992/129145133-c5965345-771d-45d8-8f63-dc8f65ff12dc.mp4 <br>

   <br>
   Files : All files related to this app are in the Application Directory. <br>
   <br>
   <br>
   References : <br>
   1. https://www.youtube.com/watch?v=HFUR9uSZFQY  <br>
   2. https://www.youtube.com/watch?v=6altVgTOf9s  <br>
   3. https://medium.com/voice-tech-podcast/android-speech-to-text-tutorial-8f6fa71606ac <br>
   
   
   
   
 
