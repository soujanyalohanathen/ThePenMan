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
   It has been noticed there were errors. And also this solution will be more applicable if the work can be done in real time.<br>
   ![audiosegmenttype](https://user-images.githubusercontent.com/58034992/129144509-84422496-f1d3-4e44-b928-284888b13b30.jpg) <br>


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
   
   <br>
<u>Update 23.09.2021</u>
   
<b>How Speech Recognition in Python Works?</b> <br>
   
  Speech must be converted from physical sound to an electrical signal with a microphone, and then to digital data with an analog-to-digital converter. Once digitized, several models can be used to transcribe the audio to text.

Most modern speech recognition systems rely on what is known as a Hidden Markov Model (HMM). This approach works on the assumption that a speech signal, when viewed on a short enough timescale (say, ten milliseconds), can be reasonably approximated as a stationary process—that is, a process in which statistical properties do not change over time.

In a typical HMM, the speech signal is divided into 10-millisecond fragments. The power spectrum of each fragment, which is essentially a plot of the signal’s power as a function of frequency, is mapped to a vector of real numbers known as cepstral coefficients(It is retrieved from the Inversed Fourier Transform). The final output of the HMM is a sequence of these vectors.

To decode the speech into text, groups of vectors are matched to one or more phonemes—a fundamental unit of speech. This calculation requires training, since the sound of a phoneme varies from speaker to speaker, and even varies from one utterance to another by the same speaker. A special algorithm is then applied to determine the most likely word (or words) that produce the given sequence of phonemes.

One can imagine that this whole process may be computationally expensive. In many modern speech recognition systems, neural networks are used to simplify the speech signal using techniques for feature transformation and dimensionality reduction before HMM recognition. Voice activity detectors (VADs) are also used to reduce an audio signal to only the portions that are likely to contain speech. This prevents the recognizer from wasting time analyzing unnecessary parts of the signal.
 
In python, there are several libraries which facilitates all the above procedures in a single package.
      <li> 1. SpeechRecognition
      <li> 2. google-cloud-speech
In my case since I am not running a Google Cloud project, I tend to use the Speech Recognition Library from Python.
Requirements :
         PyAudio 0.2.11+ (required only if you need to use microphone input, Microphone) <br>
         PocketSphinx (required only if you need to use the Sphinx recognizer, recognizer_instance.recognize_sphinx) <br>
         Google API Client Library for Python (required only if you need to use the Google Cloud Speech API, recognizer_instance.recognize_google_cloud) <br>
         FLAC encoder (required only if the system is not x86-based Windows/Linux/OS X) <br>
         Reference : https://pypi.org/project/SpeechRecognition/ <br>
In my case, I am only using my inbuilt microphone, therefore I am using puAudio Library for Voice Recognition.<br>
         
But the draw back of this is, if multiple persons speak at same time it always transcribes what it listen within that frame. Sometime this will lead to an inaccurate transcription or can end up with no results. <br>
         
         
<b>How to Send the Transcribed text to the XY Plotter ? </b>
         G-Code will be a communicator between the laptop and the XY plotter. 
         What is a G-Code ?
         G-code is a programming language for CNC (Computer Numerical Control) machines. G-code stands for “Geometric Code”. We use this language to tell a machine what to do or          how to do something. The G-code commands instruct the machine where to move, how fast to move and what path to follow.

         In case of a machine tool such as lathe or mill, the cutting tool is driven by these commands to follow a specific toolpath, cutting away material in order to get the            desired shape.

         Similarly, in case of additive manufacturing or 3D printers, the G-code commands instruct the machine to deposit material, layer upon layer, forming a precise geometric          shape. <br>
         
         Sample G Code : <br>
         ![image](https://user-images.githubusercontent.com/58034992/134470899-76f4f152-a733-46ea-92c0-5da663635e4c.png) <bR>
         
         This is the sample Gcode File I have generated from an external software called Inkscape.
       
<b>What is the Flow of the project?</b>
         1. Speech will be transcribed using Python's PyAudio Library.
         2. Transcribed text will be converted to G-Code (Not Finished yet)
         3. G- Code will be sent by G-code sender in Python via USB cable to the XY Plotter.

<b>Simulating with Coppelia Sim</b>
         CoppeliaSim has a gcode library in which we can write the code to write according to the GCode. <br>
         ![image](https://user-images.githubusercontent.com/58034992/134472218-39699050-b178-4f6d-8bd2-16b0cbee52c0.png)<br>
         
         This code gave me a simulation like this. <br>
         ![image](https://user-images.githubusercontent.com/58034992/134472425-ed2de11a-25cb-47ed-a17d-8cb9849d1e64.png) <br>
         
         And Now I am trying to communicate from my python script to the CoppeliaSim in order to Make this project in the Remote Simulation.

