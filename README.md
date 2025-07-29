# Project 7 - Task App

Submitted by: Natalie Chan

This is a task management application designed to help users organize their daily responsibilities. 
It features local data persistence using UserDefaults, allowing users to create, read, update, and mark tasks as complete. 


Time spent: 5 hours spent in total

## Required Features

The following **required** functionality is completed:

- ✅ App displays a list of tasks
- ✅ Users can add tasks to the list
- ✅ Session persists when application is closed and relaunched (tasks don't get deleted when closing app) 
  - ✅ Note: You have to quit the app, not minimize it, in order to see the persistence.
- ❌ Tasks can be deleted
- ✅ Users have a calendar view via navigation controller that displays tasks	


The following **additional** features are implemented:

- ✅ Tasks can be toggled completed
- ❌ User can edit tasks by tapping on the task in the feed view

## Video Walkthrough

<div>
    <a href="https://www.loom.com/share/30d32c4b17db4eb29f8bc98240d690df">
      <p>Loom Message - 28 July 2025 - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/30d32c4b17db4eb29f8bc98240d690df">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/30d32c4b17db4eb29f8bc98240d690df-7f8cab6436e9d094-full-play.gif">
    </a>
  </div>

## Notes

During the development process, a significant challenge arose when integrating the UITabBarController with the existing TaskListViewController and its UINavigationController.
Initially, the "Add" / ("+") button, which is crucial for creating new tasks, disappeared from the navigation bar. My immediate thought was that the button might simply be hidden or 
obscured by other UI elements. However, upon deeper investigation, it became apparent that the problem was fundamentally tied to the intricate linking between the UITabBarController, 
the TaskListViewController, and its UINavigationController. A key discovery was that the "Is Initial View Controller" setting in the storyboard was incorrectly assigned to the 
UINavigationController. The solution involved correctly designating the TabBarController as the app's initial entry point, and ensuring it properly pointed to both the 
TaskListViewController's UINavigationController (for the task list tab) and the CalendarViewController's UINavigationController (for the calendar tab) via relationship.

## License

    Copyright [2025] [Natalie Chan]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
