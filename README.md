# ST7565-ST7565P-COG-3-Inch-LCD-Library-for-STM32Cube-IDE
ST7565/ST7565P COG 3" LCD Library for STM32Cube IDE. Easy integration, versatile functionality, optimized performance. Start coding with our open-source project. Join our community for updates and support. Unlock the full potential of COG LCD displays. Happy coding!


/*************** NOTE ****************/

facebook page:

https://www.facebook.com/radioactiveengineer

subscribe to my channel:

https://www.youtube.com/@radioactiveengineer

My patreon: 

patreon.com/RadioactiveEngineer

I have poured my personal time and effort into developing this library and extensively testing it with the ST7565/ST7565P controller. To make my content more versatile and appealing, I strive to create engaging tutorials, project showcases, and informative code examples that highlight the unique benefits and features of my library. I believe in the power of visuals, so I incorporate images, diagrams, and videos to enhance the presentation and simplify complex concepts. By sharing my personal journey and experiences, I aim to connect with my audience on a deeper level, showcasing my passion and the challenges I've overcome. I value the input and collaboration of my audience, and I encourage them to provide feedback, suggestions, and ideas to further improve the library. Together, we can build a supportive community where knowledge is shared, and everyone benefits. If you find my content valuable and would like to support my efforts, please consider following my social media profiles, supporting me through my patreon or subscribing to my newsletter. Your support will enable me to continue developing and enhancing the library, ensuring its availability to all who can benefit from it.

/************** Tutorial Starts Here ***************/


Follow these steps to make this library working -> 

STEP # 01:

Add this library header to your main.h file:

#include "ST7565.h"

STEP # 02:

you can select pin of your choice I have chosen these for my program:

for the control lines I have used the following pins:

RS  -> PD8 
CS  -> PD9 
RST -> PD10

and for the data and clock lines I have used these pins:

SDA -> PB15
SCL -> PB13

STEP # 03:

add this before the loop for initialization :

  void ST7565_init(void);

STEP # 04:

Add this to your int main() function to start displaying Strings (REMEMBER TO ADD this function at the end of your display program updateDisplay(); just like I did in the example below):


	char tubewell[] = "This program is";
	ST7565_drawstring_anywhere((LCD_WIDTH/2)-((strlen(tubewell)/2)*6), (LCD_HEIGHT*3/3)-15, tubewell);
	char monitoring[] = "Developed by: ";
	ST7565_drawstring_anywhere((LCD_WIDTH/2)-((strlen(monitoring)/2)*6),  (LCD_HEIGHT*2/3)-15, monitoring);
	char system[] = "ARSALAN ALI";
	ST7565_drawstring_anywhere((LCD_WIDTH/2)-((strlen(system)/2)*6),  (LCD_HEIGHT/3)-15, system);

	updateDisplay();

STEP # 05:

ENJOY!!!!!!!!!!!!!
