# Social-distance-detector

1.Find the distance between 2 nearest person and classify them as safe (green boxed) or unsafe(red boxed)

2.Give alarm if cluster of people is identified prompting everyone to follow social distancing.

3.Send SMS alert to concerned authorities if the risk factor is found high.

--> social_dist.py

In this program, we use the captured video stream to identify whether the people are following social distancing norms.

Green box is drawn outlining the person if they are within distance of minimum 6 feet from others, 

else Red box is drawn indicating they are not maintaing a safe distnace from others.

--> social_dist_storage.py

It has all the functionality as the above program, additionally some extra features:

 1. We have added a parameter called Risk Factor(RF = #people within unsafe distance/ #people) 

 2. We store Timestamp and RF every second in a CSV file, which can be used for further analysis.

--> social_dist_bolt_sms.py

 Furthermore, in this program we have integrated Bolt IoT Wifi module to give out an alarm whenever the RF > 0.3. 

 This alarm will alert the people to maintain the social diatance. Once RF <= 0.3 the alarms stops ringing. 

 Also, if the RF > 0.5 concerned authorites will be alerted via SMS facility in our program. 

 In Addition to that, we are storing RF and Timestamp in MySQL database in this program instead of a CSV file.
