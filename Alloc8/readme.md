Below is some extra explanation for all the features implemented in the project.

1. **Login and sign up screen**  
   ![Login screen](1_login.gif)  
   This is the first page the user will see, here they can login using an existing account or create a new one. There is also validation on each input field (e.g. required, value length, format checks for email and password).
   Once the user is logged in they get a JWT token that is automatically stored so that the browser remembers the user.

2. **Calendar view**  
   ![Calendar view](Alloc8/2_calendar.gif)  
   For this project I created a calendar view from scratch, this gave me the freedom to seperate each day into 2 sections: morning and afternoon. This was good enough since a desk reservation could only be made for 3 time periods,
   namely morning, afternoon or the entire day. On this page the user can navigate through the weeks and see (both individual and team) reservations.

3. **Creating an individual reservation**  
   ![Individual reservation](Alloc8/3_individual_reservation.gif)  
   This is the part I spent most time on and I'm also most proud about. It's the workflow that enables users to make reservations for desks that they can select on a 2D floor plan (created using `Konva.js`).
   1. The user can start the workflow by selecting a time period of a certain day on the calendar.
   2. The user then has to select a segment. A segment is a part of an office such as a seperate floor or room, segments can also have sub-segments (e.g. a room on a certain floor). The user can easily navigate through the (sub-)segments inside the dropdown menu.
   3. Once a segment is selected its floorplan will be displayed, now the user gets to pick a time period for the reservation.
   4. Now the user has to select the desk for which they want to make a reservation. This is done by simply clicking on it on the floor plan, you can unselect a desk by clicking on it again, clicking on another desk or by clicking the `x` button behind the desk in the topleft window.
   5. In the last step the user get the option to make the reservation reoccur. This can be weekly and bi-weekly.
   6. Finally the user gets an overview of all selected values as a final confirmation.
  
   Once the reservation is created it will automatically be displayed on the calendar, now the user can click on the reservation to get a quick overview of the reservation data to easily check which desk was reserved.

4. **Creating a team reservation**  
   ![Team reservation](Alloc8/4_team_reservation.gif)  
   This workflow is very similar to the creation of an individual reservation.
   1. Team admins get to select a team (only teams in which they have admin permissions are displayed) for which they want to create a reservation.
   2. Then they also have to select a segment and time period.
   3. Finally they have to select desks. Individual reservations only allow selecting a single desk while team reservations allow multiple desks.
  
5. **Manage team**  
  ![Manage team](Alloc8/5_manage_team.gif)  
  Team admins can manage their team: they can invite and delete users and grant or invoke admin permissions. Inviting a user to a team is done by entering an email address, an invitation email will be sent to this email address with a link.
  The email address is first checked to see if there already is an existing account with this address. If not, the link automatically opens the signup page where the user has to register. Afterwards the user will automatically be added to the team.
   
7. **Set team color**  
   ![Team color](Alloc8/6_team_color.gif)  
   Team admins can also change the color of a team, this will change the color of reservations for the corresponding team. This way the calendar's team mode has a cleared seperation of teams. This color is automatically applied for all users.
