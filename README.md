# jaimestream

Question1.1 File:
For the first point in exercise 1, this source code is gooing to let us implement a small example for the streaming of Level3 HLS stream and Cloudfront HLS stream. As a basic result we should be able to visualize the video and also the Streamroot Graphs.

For the second point in exercise 1, if you want to generate a P2P between 2 different URLs  you have to add contentIdGenerator. For this you need to create two indepent files but with the same source code, the first one for the Level3 HLS stream and the second file for the Cloudfront HLS stream. To do this, you need to add "contentIdGenerator" : contentIdFn, in line 66 in both files (Question1.1 and Question1.2) and create a function on both in line 22. By default line 66 is commented (//) in both files, so it doesn't execute it, but all you have to do is uncomment it for it to work.

To implement a button to enable/disable P2P upload you need to create a function, in this case I called it "setuUpload" with two different conditions as it is presented in line 26 in the Question1.1 File. To create the button you need to add <button id="btnUpload" onclick="setuUpload();">Stop upload</button> in line 49. It is commented by default so you need to uncomment it to make it function. 

EXERCISE 2:

In this exercise you can see there is a 403 error with the link https://cdn.streamroot.io/latest/dna-client/5.30.1/dna-client.js. The 403 Forbidden Error happens when the web page (or other resource) that you’re trying to open in your web browser is a resource that you’re not allowed to access. Why this happened? Well apparently there isn't any error with the source code but after searching through Streamroot's documents data base in the website, we can see that the dna-client.js file that was is being used by the customer it is out of date and that since v7.2.1, Flowplayer has an integrated interface to the hls.js client library. To solve this we need to change "lib/flowplayer-hls-dna-plugin.js?srKey=da32565b-dd31-4ae8-9be7-951d6ca79621" for "https://cdn.streamroot.io/flowplayer-hls-dna-plugin/1/stable/flowplayer-hls-dna-plugin.js?srKey=da32565b-dd31-4ae8-9be7-951d6ca79621".  
