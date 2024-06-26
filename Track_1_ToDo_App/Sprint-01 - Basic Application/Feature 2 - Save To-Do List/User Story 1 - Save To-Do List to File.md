# 📖 User Story: Save To-Do List - Step-by-Step
⏲️ _Est. time to complete: 15 min._ ⏲️

## User Story

*As a user, I want to be able to have my to-do list automatically saved to a file when I exit the program.*

## 🎯Acceptance Criteria:
- A file is created when the program exits that contains the to-do list items.
- The file will be a ".txt" file
- each line in the file will contain a single to-do item.

## 🎓Know Before You Start
The following resources/videos will help you get a better understanding of some of the basic Python concepts that you will use to complete this user story.
- [Working with Files](https://youtu.be/uQ5BZht9L3A?t=5812) (~ 1 min)

## 📋Steps

In order to complete this user story you will need to complete the following tasks:

### Start your Codespace or Open Visual Studio Code locally
<details>
<summary>click <b>here</b> if you are running in Codespaces</summary>

If you are using a Codespaces, please go into the repo that you created for this project and start the codespace by directly clicking on the Codespace name.  In the case of the image below, the Codespace is named _symmetrical computing-machine_. Note however, that each Codespace auto-generates a unique name for that code space so your Codespace name will be different.  

![Start Codespaces](/Track_1_ToDo_App/content-images/github-start-codespace.png)

This will take you directly into a online visual studio code environment.

![online visual studio code](/Track_1_ToDo_App/content-images/github-start-codespace-02.png)
</details>

<details>
<summary>click <b>here</b> if you are running Visual Studio Code in a local development environment</summary>

- From the terminal/console window, navigate to the project directory
  
    ```bash
    cd <project directory>
    ```
- Open up Visual Studio Code in the project directory by executing the following command.
    
    ```cmd
    code . 
    ```
</details> 

<br/>

Open the `app.py` file in the root of your project folder.

<br/>

### Updating the code base for new functionality

#### 1. Update code to save to file on exit
The one change that we will need to make to the code is to update the logic for the exit functionality. We will need to add code that will save the to-do list to a file when the user selects to exit the program.  Add the following code to the `if` statement that checks if the user selected to exit the program (see code example below).

>[!TIP]
>You can use GitHub Copilot to make this code change. Use a prompt like *update to save todo list to file on exit*

```python
#user selected 'x' or 'X' - To Exit the program
if choice == "X":
    # Save the to-do list to a file
    #**********THIS CODE ****************
    with open("todo_list.txt", "w") as file:
        for todo in todo_list:
            file.write(f"{todo}\n")
    #************************************
    break
```

This code will open a file named `todo_list.txt` in the current application directory and write each item in the `todo_list` to the file.  The `w` parameter in the `open` function tells Python to open the file in write mode.  This will overwrite the file if it already exists.  The `for` loop will iterate through each item in the `todo_list` and write it to the file.  The `\n` character is used to add a new line to the file after each item is written.  This will make the file easier to read when you open it in a text  editor as each to-do item will be on its own line.

<br/>

#### 2. Run the application
Now let's see this application in action. Open the terminal and navigate to the folder where your `app.py` file is located. Run the application by typing `python app.py` and pressing the enter key or simply click the play button in the top right corner of the Visual Studio Code window.

- Add a few items to the list and then select 'X' to exit the program.
- Within Visual studio code, you should now see a file named `todo_list.txt` in the same directory as your `app.py` file.
- Open the `todo_list.txt` file in the same directory as your `app.py` file. You should see the items that you added to the list in the file.

![RunApplication04](/Track_1_ToDo_App/Sprint-01%20-%20Basic%20Application/images/RunApp-S1-F2-US01-01.png)

<br/>


> [!NOTE]
> 📄For the full source code for this exercise please see [here](/Track_1_ToDo_App/Sprint-01%20-%20Basic%20Application/src/app-s01-f02-us01/app.py).

<br/>

[🔼 Home ](/Track_1_ToDo_App/README.md) | [**◀ Previous user story**](/Track_1_ToDo_App/Sprint-01%20-%20Basic%20Application/Feature%201%20-%20Manage%20Todo%20List/User%20Story%202%20-%20Remove%20Item%20from%20List.md) | [**Next user story ▶**](User%20Story%202%20-%20Load%20To-Do%20List%20from%20File.md)