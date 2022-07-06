# Changelog
Additions and updates to the Memseer
{: .fs-6 .fw-300 }
---
### Version 22.7.6:
**Bug fix: incorrect spelling of email notification subject**

_Incorrect_: "Late: something past due by 1 days!!!"

_Correct_: "Late: something past due by 1 day!!!"

**Add: documentation link**

Link to documentation has been added to sign up page and in-app menu

**Remove: quick action from quick event**

Presence of quick action button during quick event is confusing, since quick event typically originates from existing action, 
therefore, there is no point of adding or looking up the action. 

**Change: email notification subject**

Email notification subject will contain ⚠️ instead of !!!.

### Version 22.6.23:
**Bug fix: incorrect units of work during import of an item**

The bug occurs when you import an item with units of work such as hours or kilometers.
Units of work are disregarded and set to "miles" instead.

### Version 22.5.16:
**Bug fix: origination date**

The bug occurs when you set origination date of an item in to the future.
Item schedule calculates incorrectly and provides user with bad information.

Now user can't pick a date in the future, only in the past. However, there is a manual override, which is not restricted at least for now.

### Version 22.5.2:
**New feature: insufficient units of work**

Now maintenance card displays an action due to insufficient units of work data (such as kilometers/miles/hours) .
In order to have proper schedule calculated, the maintenance card asks user to fill out current units of work.

Steps:
- Create new item with 'work units' and action/s with a unit of work (ex. miles)
- Given there are no prior events associated with the action
- Navigate to dashboard and find the item, it should have a task with red icon, noting that sufficient information, 'please add current miles'

### Version 22.4.23:
**New feature: maintenance card items for actions with insufficient events**

Now maintenance card displays actions that can't be calculated due to insufficient event data.
In order to have proper schedule calculated, the maintenance card asks user to fill out past events.

Steps:
- Create new action in new or existing item
- Given there are no prior events associated with the action
- Navigate to dashboard and find the item, it should have a task with red icon, noting that sufficient data is missing for the action


### Version 22.3.29:
**New feature: notes for actions**

Now you can add notes to action, for example: include specification about the action.

Steps:
- Create new or go to existing item
- Add new action or find exist one
- Click on 'notes' icon
- Fill in any notes (example: 'make sure bolt is tighten to 75 foot pounds')
- Click on 'save'

**Bug fix: import of unsupported formats**

The bug occurs when you import a file of unsupported format, for example: .jpeg or .pdf
Supported import formats are:
- json - for item and actions import
- csv - for events import

Now software is explicit about what kind of file can be imported and does not allow empty events or actions.

### Version 22.3.19:
**Bug fix: mismatching events and actions**

The bug might occur when importing/exporting events and items.
Events and actions stop associating, preventing correct scheduling.

**Bug fix: no more undefined in action-event tooltip**

The bug doesn't do any harm, but visually confusing.
Tooltips should not present any 'undefined'.


### Version 22.3.12:
**New feature: work hours**

Now you can record working hours of any equipment, for example: treadmill

Steps:
- Add new item
- Give it a name, example Treadmill Pro 2000
- Enable 'work units', new dropdown box will appear
- Select 'hours'
- Now you can keep track of work hours of the treadmill
