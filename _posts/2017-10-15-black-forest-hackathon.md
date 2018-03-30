---
layout: post
title: Blackforest Hackathon 2017
image: /img/bfh.png
tags: [hackathon, black forest, digital assistant]
---

Last weekend I participated in my first hackathon in Offenburg, Germany. The [Blackforest Hackthon](http://www.blackforest-hackathon.com)'s topic was to create a digital assistant. Our goal was to develop an assistant that could recognize people via face recognition and display certain information according to the person's priorities.

After having some issues with OpenCV's face detector, we decided to move on with dlib's detector and train an own SVM instead of using OpenCV's predefined modules. Even with few training images and a shallow machine learning approach, we already had some good results as shown in the image.

![picture of the team](https://img1.picload.org/image/dgccigci/bildschirmfoto2017-10-08um02.2.png)

The next step was to acquire the needed data, where we used google-api-python-client to access mails and calendars. For displaying news, we used BeautifulSoap to extract the information out of the HTML content. Using the OpenWeatherMap web API, we got the current weather information. To make the communication with the application easier (also for impaired people) we decided to use Google's Speech Recognition API and the text-to-speech x-platform for speech synthesis.

![our team presenting](/img/blackforesthackathon.jpeg)

To implement a GUI, we were using PyQT5 that gave us some problems as we lacked experience there. Nonetheless it was a great weekend, where I met a lot of nice new people and had a fun time working on an interesting project.

Feel free to check out the source code [here](https://github.com/manu183/BlackForestHackathon).
