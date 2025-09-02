This app helps you track your daily nutritional intake by querying a large language model. Enter a food item with a quantity (e.g., "1 large banana") and the app will add it to your log and update your daily totals. All data is saved automatically in your browser's local storage.

This application can use the Gemini API (or another LLM API) to get nutritional information. To use a custom API key, you can get one for free from here: https://aistudio.google.com/app/apikey. You get more than enough free calls per day with Gemini. 
Clicking the default button will auto-fill a link to pollinations.ai which doesn't require a key, but is not as accurate. If you don't know what an API key is, then just click `default`.

## Main page
- Click through to see previous days
- Daily counts and targets are displayed. If you use Macrodroid or Tasker then you can grab the screen contents easily.
- Enter any food item in plain English, e.g .`a small bowl of cereal with milk`, `2 slices of bacon`, `a very greasy slice of cheese pizza`, `35g grilled chicken breast` and either click `Add Item` or just enter on your keyboard.
- You can also submit multiple items separated by commas as a single entry, like `3 pancakes, a cheeseburger, four tacos, and a diet coke`, though the data returned will be less accurate.
- Version 3.5 added camera support. Try to keep your food in clear view without other objects in the shot. Not all LLM APIs accept images.
- The entry is immediately listed as `pending` and a call is made to the LLM API to fill out the calories and macros.
- If an item seems stuck as `pending` you can click it to try again.
- If there are data errors - either the LLM isn't returning properl formed data or your connection is weak - then you can edit an item to manually add data.
- If you change the name of a previously added food item then it's re-sent to the LLM for recalculation.
- `Analyze My Data` will send you entire saved history and entered goals to the LLM to provide a (hopefully) gentle, positive analysis of your eating habits. If you have a history of disordered eating then this is best done in consultation with your doctor and therapist, not with an app.
  - This won't be very useful until you have at least a couple weeks of data.


## Settings
- Enter you daily calorie target. Reasonable macronutrient target are auto-computed. 
- Nutrition goals are optional and can be entered in plain English.
- `Use local cache for previous foods` will check previously entered food items and populate the calories and macros without using the LLM, so check this if you enter the same item often.
- Make sure to save your API settings, but remember your API Key will be saved here in plaintext, so don't share it with **anyone**.
- Anything you add in `Morning Food Automation` will be added to your daily food diary once per day when you open the app.
- `Data Management`
  - Settings and your record of food items are stored locally in your browser. There is no server, no data is shared. So if you clear your browser's cache then it's all gone.
  - Exporting your settings will save them to a file in your default downloads folder, to be imported if your cache is cleared.
  - You can export your history of entered items as a CSV file that you can open in a text editor or spreadsheet app. Do this from time to time so you don't lose your data when you inevitibly clear your browser's cache. Then import it again.
  - `Clear All Data` wipes the cached data in the app.
