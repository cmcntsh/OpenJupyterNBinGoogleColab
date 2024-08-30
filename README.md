# Open a Jupyter Notebook in GitHub Using Google Colab

* Copy the url of the GitHub repository you want to use.
* Go to https://colab.research.google.com/
* Click on the GitHub heading on the left (#1)
* Paste the GitHub repository url in the space provided (#2)
* Click on the notebook you want to open (#3)

![image](https://github.com/user-attachments/assets/d3a6c437-bf69-40a4-83d3-e1ebe6021838)

* If your repository has data files you want to use, you may want to clone the repository

```
!git clone <your GitHub repository url> # replace the address shown with the address to your own repository
```

# Get the path to your data

* Get the path to your data by hovering over the three dots next to your data file and select copy path from the dropdown

![image](https://github.com/user-attachments/assets/aa3d6c12-c2f7-4c8f-ad4f-0d2089679527)

* You can use that path in your code cells

```
original_files_path = '/content/sample_data/california_housing_test.csv'
```

# Push updated data to GitHub

* You'll need to generate a personal access token for GitHub
* https://github.com/settings/tokens/new
* I gave it a name like 'GoogleColab2'
* I set a custom expiration of 1 day. (You can always make another. People can do bad things if they get ahold of your access token.)
* You can also just go delete the access token after you use it to upload your assignment to GitHub. (I highly recommend doing this. Just leave the page with your access token open while you complete the rest of the steps to push your data to GitHub. After you do that, go to the access token page and delete your access token. Then there's no chance of misuse.)
* I just checked the repo box and that was all.

![image](https://github.com/user-attachments/assets/1be51f05-ea29-449c-8d95-333772610660)

* Scroll all the way down the page and click the button to create the token
* Copy your token. You'll need it for the code to push to GitHub

```
!git config user.name "<GitHub user name>"
!git config user.email "<GitHub email>"
!git status
!git add .
!git commit -m "adding data"
#!git push https://<YOUR-PERSONAL-ACCESS-TOKEN>@github.com/<User-Name>/<Repo-Name>.git
!git push https://<your access token>@github.com/<GitHub user name>/<GitHub repository name>.git
```

# Export your notebook with output if you want to save it.

* Pushing your new files to GitHub doesn't update the Google Colab notebook in Github.
* You'll need to export your completed notebook and manually upload that to your repository.
* Google Colab - File - Download - Download .ipynb
* GitHub - Upload file

![image](https://github.com/user-attachments/assets/f4636ce9-d840-4df1-a975-90c6ca3aadbd)
