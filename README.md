How to Dynamically Add New Data to the Game
Follow these steps to add new data dynamically to the game:

1. Update the FileVersion.json
Add a new entry in the FileVersion.json file with the category name and the corresponding version number.
Example entry:
json
Copy
Edit
{
  "CategoryName": "NewCategoryName",
  "CategoryVersion": 1
}

2. Add a New Data File in the WordData Folder
Create a new file in the WordData folder with the same name as the CategoryName added in the FileVersion.json.
Populate the file with the new data using the pre-defined structure.
Ensure the structure follows the existing format to maintain compatibility.

3. Automatic Update and Merge Process
The game will automatically:
Compare the local copy of FileVersion.json with the GitHub copy.
If a new category is found or if the version of an existing category has been updated:
It will merge the updated word data into the local version.
If the category is completely new, it will add the new file to the local WordData folder.

Important Notes:
Ensure all data files are properly formatted to avoid runtime errors.
Keep the FileVersion.json on GitHub updated with the latest changes to reflect the new data categories and versions.
By following this process, the game dynamically keeps the word data up-to-date with minimal effort.
