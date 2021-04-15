# The Impact of Climate Change on Natural Disasters

https://6859-sp21.github.io/a4-usa-natural-disasters/

Throughout this assignment, our goal was to show the impact of climate change on natural disasters (particularly focusing on the last 55 years) without cluttering the interface. 

We wanted the headline of the visualization to be centered and in the biggest header font to immediately tell the viewer what the visualization is about; in addition, it includes the years represented in this visualization so that the users would not think that it is only for the single year shown on the top of map (1965). On the left side, there is a short paragraph explaining a bit more about the visualization and its intention; we also wanted to allude to the meanings behind each component in the visualization, such as explaining the meaning of colors behind each state and also guiding the viewers to the legends for reference. Since this short paragraph could obstruct the map view depending on the user's window size, we made this collapsible (default is open, so that the viewer can easily locate/realize it). There are also sources and credits at the bottom of the page. 

The main part of the visualization is the choropleth, and almost all other components support this map. As mentioned in the short paragraph to the left, the color for each state within the map represents the number of natural disaster declarations that happened in that state in a particular year. As the viewer can see from the top-right legend, the disaster count ranges from 0 to upper 700s, with the darker, more prominent colors inferring more disasters in that state/year. Red/Orange colors were chosen for this scale as they often represent warning and danger. Hovering over a state also displays the exact count of natural disasters that happened in that state that year; we are hoping that the color scale provides an idea of the number of disasters that happened in a state, and if they are interested, they can find out the exact number by hovering over the state. 

The user is able to interact with the map in several ways. First, the slider at the bottom allows the user to toggle between years to see how the disaster patterns change over the years. Upon changing the year on the slider, the current year selected shows up at the top of the map in the form “Year: ####”, making it clearer to the user what year they are currently viewing. The slider also has a timeline on top, noting significant natural disasters that happened in the last half a decade. When a user selects years such as 2005 or 2020, they might wonder what happened in those years; our hope is that these selected events might provide the viewers with a bit more context for some years. 

Our second element of interaction enables users to click on a state within the map. Upon clicking on a state, there is 0.5 second animation that leads the viewer to a zoomed in view of the selected state. Clicking on the selected state again or clicking on the body of water (if the selected state is close to a body of water!) would zoom out of the current selection and reset the view to the full map. Upon zooming into a state, the user would be able to see dots/circles. These dots are plotted on the locations where disasters happened, if the dataset contained affected county information on a specific disaster. Each dot represents a reported disaster, and upon hovering over a dot, information about the disaster is revealed in a tooltip: exact date of the incident, type or name of incident, and the county details. In some cases where multiple disasters happened in the same county within the same year, we offset the location a bit so that hovering over and noticing distinct disasters in the same county would be a bit easier. 

Third, the user is able to filter out specific types of natural disasters using the checkboxes on the right. If the user is not zoomed into a specific state, the entire map would change colors depending on the number of disasters for the selected categories. If the user is zoomed into a specific state, only the dots corresponding to the selected colors/types on the legend would show up. By using the filtering function, the user is easily able to see which state has a high concentration of which type of disasters and any sudden increase of specific type of natural disaster between years. 

There were some things we considered adding into the interface, but decided not to. In the MVP, we had a popup modal that gets activated upon a click on a disaster dot. In the MVP, we got some comments that though they liked the popup for more information, the current modal did not contain much more information than what is in the dot tooltip already. We would have loved to include information such as casualties and cost damage, but the dataset we chose unfortunately did not include much information beyond what we already provide in the tooltip. In order to keep the interface simple, we have decided not to include the clickable modal in the final submission. We also initially had the disaster dots showing up on the map the entire time, and in the end we just decided to have the dots only when the user selects a specific state, and show the dots only for that state, not others. The loading of dots between years was consuming too much load time, slowing the slider brushing very much; in addition, the constant existence of dots was commented to be a bit overwhelming from the feedback we got from classmates. We also considered using icons instead of colored dots to represent disasters, but the load time for the icons was long and we decided that it would affect the user experience negatively. 

One last thing we would like to note is that this was a difficult dataset to visualize. Though the usability of the data was good, we realized that this dataset might require more expert knowledge in environmental science. For example, some people believe the COVID-19 pandemic to be caused by climate change, but this cannot easily be proven and could be a subjective opinion. Throughout the assignment, something we struggled with was deciding what is a natural disaster caused by climate change—earthquakes, for example, is the increase in earthquakes caused by man-made climate change or by increased seismic events? We also did the best in our ability to classify disasters into categories such as “water” and “fire”, but we might need some expert in the field to check our classification of disasters as well. Additionally, the dataset had limited information about the magnitude of impact of these disasters, exact latitude and longitude coordinates (so we had to look up generic coordinates for counties or states), and other information that would be helpful to provide context for natural disasters; these would be great ways to further improve on the detail and context of our visualization. 

Kalyn and Helen worked on the map, with Kalyn focusing more on state-level information and Helen focusing more on county-level information. Yuji worked on a lot of the design and appearance, including the time slider which was polished in functionality and the significant natural disasters added by Kalyn later on. The styling and functionality of the legends/checkboxes were worked on by Helen and Yuji. 

In total, we together spent roughly 40 hours. The map took a lot of our time, such as connecting it to the checkboxes and selecting the correct county (since multiple states could have the same county name). 
