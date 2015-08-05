####Multiple Date Picker in UITableView static Cells

This is a comman requirement in many applications to diplay multiple date picker in table view
and luckily there is a simple solution for that below are the steps to acomplish it

1 - Create a table view controller with x*2 static cells where x is number of date picker required.
2 -	Create the first cell as a date holder with type of subtitle
3 - Create outlet for detail lable of cell which will hold the date.

4 - create the second cell of height 165 and place a datepiker inside it and create an outlet and action for datepicker date change

5 - Repeat step 2 to 4 for second cell

6 - In table view controller implement cell for row at indexPath and didSelectRowAtIndexPath method in such a way that if the 1st or 3rd row get selected make 2nd or 4th row flag visible.
7 - implement heightForRow at indexPath method where return 165 if the visible flag is true for 2nd or 4th row.
8 - implement method for dateChange IBAction implemented for datepickers in a way that when value change it updates the 1st or 3rd row subtitle label.
