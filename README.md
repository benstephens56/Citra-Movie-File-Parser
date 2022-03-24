# Citra-Movie-File-Parser
This code can be used as a template file with 010 Hex Editor in order to easily parse Citra movie files (.ctm). It will organize the data into frames, and within each frame, inputs will be broken up into the different controller state types.

010 Hex Editor is a paid hex editor program with a lot of functionality. Despite being a paid program, there is a 30 day free trial. Once this free trial has expired, the program can be uninstalled and reinstalled to regain access.

In order to use this template file, first open a CTM file in 010 Hex Editor. This should open the hexidecimal data for that file. Now go to Templates -> Open Template (Ctrl + F5) and open CTM_Template.bt. This will color code the hex data at the top of the page by frame and data type. 

At the bottom of the window, in the Template Results area, there should be two fields with drop down areas labeled as "Header" and "Inputs." The header results contaisn metadata contain in the movie file such as the author, frame count, total movie time.

Under the inputs results, every frame is listed with a dropdown menu. Within the dropdown menu for each frame are listed each input type that was recorded in that frame. The different input types are as follows:
  - Pad & Circle: Base model 3DS buttons and circle pad inputs
  - Touch Screen
  - Accelerometer
  - Gyroscope
  - New 3DS: ZL, ZR, and C-Stick inputs
Within the value column of each dropdown lists the input recorded for that frame. A note that not all inputs types will be recorded every frame or in every movie file. For digital inputs, the For instance, if a specific game doesn't use any New 3DS inputs, the New 3DS dropdown menu probably will not appear in the results. You can edit each input from the results menu. This is especially useful for analog inputs as they can be changed using decimal in the results panel despite being recorded as hex in the actual file data.

My code is a mess and but thus far it has worked for every CTM file I have ever tried to play, save for 1 which I suspect is a corrupted file. I would like to continue working to imrpove this code.
