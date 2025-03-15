java c
Academic Year: 2024/25
Assessment Introduction:   
Course: BEng (Hons) Electronic EngineeringModule Code:   EL1242   Module Title: Digital Electronics   Title of the Brief: Prototyping of A Primary Smart Home System
Type of assessment: CourseworkThis Assessment Pack consists of a detailed assignment brief, guidance on what you need to prepare, and information on how class sessions support your ability to complete successfully. You’ll also find information on this page to guide you on how, where, and when to submit. If you need additional support, please make a note of the services detailed in this document.How, when, and where to submit:The deadline for this assessment is 21st      March 2025   at 23.59   via the submission zone found the EL1242 Blackboard area - Please note that this is the final time you can submit – not the time to submit!If your work is submitted via the Turnitin link on Blackboard, the link will be visible to you on: 12th   December 2024Feedback will be provided by: 26th   April 2025You should aim to submit your assessment in advance of the deadline.Note: If you have any valid mitigating circumstances that mean you cannot meet an assessment submission deadline and you wish to request an extension, you will need to apply online, via MyUCLan   with your evidence prior to the deadline. Further information on Mitigating Circumstances via this link.We wish you all success in completing your assessment. Read this guidance carefully, and any questions, please discuss with your Module Leader or module team.Additional Support available:All links are available through the online Student Hub1.   Academic support for this assessment will be provided by contacting Zengdi Bao or Xinliang Chen2.   Our Library resources   link can be found in the library area of the Student Hub or via your subject librarian at [email   protected].3.   Support with your academic skills development (academic writing, critical thinking and referencing) is available through WISER on the Study Skills section of the Student Hub.4.   For help with Turnitin, see Blackboard and Turnitin Support   on the Student Hub5.   If you have a disability, specific learning difficulty, long-term health or mental health condition, and not yet advised us, or would like to review your support, Inclusive Support can assist with reasonable adjustments and support. To find out more, you can visit the Inclusive Support page of the Student Hub.6.   For mental health and wellbeing support, please complete our online referral form, or email [email   protected]. You can also call 01772 893020, attend a drop-in, or visit our UCLan Wellbeing Service      Student Hub pages   for more information.7.   For any other support query, please contact Student Support   via [email   protected].8.   For consideration of Academic Integrity, please refer to detailed guidelines in our policy document . All assessed work should be genuinely your own work, and all resources fully cited.    9.   For this assignment, you are not permitted to use any category of AI tools.
Preparing for your assignment.Ensure that you fully understand the requirements for the assessment and what you are expected to complete. The assignment will be introduced in the lecture session where you can ask any questions, you can also ask for clarification by contacting the module team.The following module learning outcomes will be assessed in this assignment:·   Explain the operation of a basic microprocessor system, relating the description to the architecture of the processor.·   Interpret assembly language software used in the processor based system.Please read over the guide to writing a technical document https://www.theiet.org/media/5182/technical-report-writing.pdf   and ensure that you fully understand the requirements of the assessment. There will be a lecture session on the assignment and writing a technical document.Ensure that you research and read into the subject area before writing the report so that you have a good background understanding to the subject area.
Assignment Brief
1.   Introduction
In   this   assessment,   the   student   will   demonstrate   the   ability   to:
·   Explain   the   operation   of   a   basic   microprocessor/microcontroller   system,   and   interpret   software   used   in such a system.
·   Write   and   test   simple   programs   using   a   modern   programming   language   and   an   appropriate   set   of development tools or environment, including use of libraries, debug tools etc.
·   Develop   digital   systems   and   programs   for   basic   engineering   applications.
·   Design   hardware   and   software   to   meet   the   specification   for   a   simple   processor-based   system.2.   Assignment   BriefSmart home devices are a part of the larger concept of home automation.   Large smart home systems utilize   a   main   hub   or   controller   to   provide   users   with   a   central   control   for   all   of   their   devices.   These   devices   can include   lighting,   heating   and   air   conditioning   and   security   system.   The   other   key application   of   smart   home   is to   provide assistance   for disabled   and   elderly individuals.   For example,   they can be   equipped with   additional safety features which include sensors that monitor for medical emergencies such as falls or seizures.   Smart home technology can provide users with more freedom and a higher quality of life.Your   task   is   to   implement   a   primary   smart   home   system   which   can   automatically   control   the   heating   and   lighting system, detect people’s falls, and provide readings of environmental parameters, e.g. temperature, ambient light levels.You   will   use   the   Nucleo   STM32L476RG   ARM   board   and   specially   made   sensor   board,   an   application   shield, shown in Figure 1.Figure   1.   Nucleo   STM32L476RG   ARM   board   and   the   specially   made   sensor   board.   3.   RequirementsSpecific   requirements   of   the   systems   are   as   follows:·   Task 1: Automatic heating control. This is about a design of a thermostat. The state of the thermostat controller is represented by a servo. When the temperature is greater than or equal to 25oC, the servo should be at a position of 0o degree, which means the controller is ‘off’. When the temperature is below 25oC, theservo should be at a position of 135o degree, which means the thermostat controller is ‘on’.·   Task   2:   Automatic   lighting   control.   Use   the   four   red   leds   as   lighting   devices.   There   are   five   required   levels of lighting, 1, 2, 3, 4 and off. The lighting level is controlled by the lightness/darkness detected by the LDR sensor, for example when it is very light, all the leds will be off, and when it is very dark all the four leds will be   on.   All   the   5   levels   of   lighting   will   be   corresponded   to   the   evenly   distributed   ‘ReadIn’   value   from   the   LDR.·   Task 3: Detecting falls. Use the 3 axis (X, Y, Z) accelerometer to detect fall and the three-colou代 写EL1242 Digital Electronics 2024/25
代做程序编程语言r led to represent an alarm. Assume that when people fall, the value of acceleration is greater than 1.8g or less than-1.8g in any direction of X, Y and Z. When a fall happens, light up the three-colour leds in turn and each colour duration time is 0.2s.·   Task   4: Environmental   parameter   readings.   Use   the   blue   User   Button   and   switches   to   control   the   content of   readings.   When   the   blue   user   button   is   pressed,   and   the   switch   position   is   ‘0001’,   display   the   temperature on the PC screen through the on board serial port. When the blue user button is pressed, and the switch position   is   ‘0010’,   display   the   relative   ambient   light   levels   with   row   of   ‘*’   on   the   PC   screen   (length   determined by   brightness).   When   the   blue   user   button   is   pressed,   and   the   switch   position   is   ‘0100’,   display   the   values   of acceleration   of   3   directions   on   the   PC   screen.   When   the   blue   user   button   is   pressed,   and   the   switch   position is ‘1000’, display the output voltage value from the potentiometer.   When the switch value is others, display a message of ‘invalid switch value’ on the PC screen.   The summary of readings is as Table 1 below,
State   of   Blue   User   Button
Value   of   Switch
Content   to   Display   on   PC
Pressed
0001
Temperature   (   oC   )
Pressed
0010
Ambient   light   levels   as   a pattern of number of ‘*’
Pressed
0100
Values   of   acceleration   of 3 directions
Pressed
1000
Output   voltage   value   from the potentiometer
Pressed
Other   values
‘Invalid   switch   value’
Not   pressed
Do   not   care
Keep   previous   display
Table   1:   Summary   of   environmental   parameter   readings
4.   Details   of   devices   on   the   specially   designed   shield.
The   details   about   the   pin   names,   connections   of   devices   are   listed   in   Table   3.Table   2:   Details   of   devices   on   the   specially   designed   shield.
5.   Development   Report
Part   of   your   submission   is   a   technical   report   about   the   development   of   the   monitoring   devices.   Within   the   report ensure that you cover the following aspects:
·   Researched   background   into   microcontollers.
·   Researched   background   into   sensors,   actuators   and   other   components   used   in   the   tasks   required.
·   Details   of   design   analysis   for   all   the   tasks.
·   Individual   testing   on   implemented   tasks.
·   Appropriate   images   and   references   of   the   development.
·   Conclusions.
Word limit: A maximum of 1000 words (see notes below for further information).
Technical Report WritingTo complete the report, you will have to thoroughly research the area using reliable sources and precisely reference where your information and statements are from. The aim of the report is to be clear, concise and convey technical information to the reader, note that the reader is familiar and experienced in the area. Ensure that you write your report for this audience.A guide on writing a technical document can be found at the following (this will also be uploaded to blackboard):https://www.theiet.org/media/5182/technical-report-writing.pdfPlease read over the above document to ensure that you are clear on what a technical report is and know what you are required to complete, note the above is a guide not an explicit standard you will be required to ensure that your technical report contains the relevant information presented correctly for the reader.Ensure that you research and read into the subject area before writing the report so that you have a good background understanding to the subject area. You will need to provide a short report, which shows the calculation of each tasks in Marking Criteria and Weighting   section below with an appropriate assumption, description and comments, no longer than 1,000 words. You should use the guideline below to structure your report. For the final reporting submission, make sure that each page is marked with the date of completion, the page number, and the total number of pages submitted.    Make sure that the front page of your submission has this information displayed prominently along with the module name and number and assignment title. Your work must be referenced using Harvard Referencing system available here: https://v3.pebblepad.co.uk/v3portfolio/uclan/Asset/View/Gm3mmGk6sM3RgHZnjGfh7mm6pM.Further information to support your development will be available to view on assignment briefing session and Blackboard.   

Notes on Wordcount and ReferencingFor good marks and given the limited wordcount you should produce work that is: accurate; thorough; well-argued; clear; accurately referenced; relevant and written in correct (UK) English grammar and spelling. You may include figures and tables with short captions (25 words each) and a list of references without affecting the overall word count. Remember that you have limited words so ensure that you “stick to the point” and do not get into detail on superficial elements.Ensure that you include references when discussing technical facts and statements on the technology used. You must reference all your sources of information. These should be cited in the appropriate part of the report and fully identified to meet the Harvard referencing standard in a list at the end. Website articles must be properly referenced to be considered as legitimate references.
Presentation of assignment work
Except where specifically stated in the assignment brief, assignment work submissions should be word-processed, in Microsoft Word 2016 format, with a footer comprising: your module code; date; page number.
The following module learning outcomes will be assessed in this assignment:·   Explain the operation of a basic microprocessor system, relating the description to the architecture of the processor.·   Interpret assembly language software used in the processor based system.   
Marking Criteria and Weighting
It is recognised that not everyone will be able to meet all of the specifications given overleaf, so the assessment scheme is designed to measure how much of the specification you can meet. You will be required to write a short evaluative report and give a demonstration of your system by taking a 20 second selfie video. All the program with inline comments you made should be included in the report as an appendix (not part of page count). Marks will be awarded as follows in Table 2.
Your submission will be marked in accordance with the following marking scheme:
Item
Possible Mark %
Task   1:   Automatic   heating   control
20
Task   2:   Automatic   lighting   control
20
Task   3:   Fall   detection
20
Task   4:Environmental   parameter   readings
20
A   20   second   video   demonstrating   your working system
20
Table   3:   Summary   of   awarded   marks.
            
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
