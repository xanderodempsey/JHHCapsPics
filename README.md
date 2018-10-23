# Genetic Emphasis
## Setup
1. Install the latest version of node.js from https://nodejs.org/en/download/

2. Install MySQL Workbench from https://dev.mysql.com/downloads/workbench/

3. Clone the repository
    ```
    git clone https://github.com/xanderodempsey/JHH_Capstone/
    ```
4. Install required libraries
     ```
    cd ~/PATH_TO_PROJECT/ && npm install
    ```

5. Open MySQL Workbench and enter the Local instance MySQL router.

6. Right click under Schemas > Create Schemas
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/CreateSchema.png)

    Name the schema jhh_capstone

7. Double click on the new schema and open a new SQL Editor. Enter in the following queries:
    ```
    CREATE USER 'jhh_admin'@'localhost' IDENTIFIED BY 'jhh123';
    GRANT ALL ON *.* TO 'jhh_admin'@'localhost';
    ```

8. Then run the data.sql file from JHH_Capstone/code/judd in a new MySQL editor.

## Using Genetic Emphasis
To run Genetic Emphasis open the node.js command prompt and:
```
cd ~/PATH_TO_PROJECT/ && nodemon index.js
```
and in your browser of choice goto localhost:3000

### Public Site
The first thing you seen once link is opened you will be presented with the home page.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/Homepage.png)
From here, a general vistor to the site can access the documents hosted as well as searching for documents by tag.

The following picture is what a user will see once accessing a document (this example is a journal article, and because of copyright issues cannot be hosted physically on the site. So a DOI is given instead.)
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/Document.png)

### Admin Login

To access the other features of the site requires an Admin login, this can be done by accessing the link at the bottom of the site. Once clicked,you will be redirected to the following page.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/adminlog.png)

Once logged in, you will get redirected to the same page. Although the user now has access to the Admin Features: Upload, File Manager, Social Media Tracker, Users.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/adminhome.png)

### Uploading Files
Click on the Upload option in the top menu. This redirects to two options: upload a File, or Link a Document.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/UploadOptions.png)

In the file upload, the user needs to choose a file from their directory, add a display name that the end user will see, and as many tags as you wish.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/uploadfile.png)

Similar to uploading files, to link a document you simply need to add the link in the text field, then follow the same procedure. *Please note that for a URL you must proceed the link with https:// and for a DOI https://doi.org/*
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/uploadlink.png)

### Managing Files
The File Manager tab looks identical to the Document menu, except now when you access the documents you get taken to a page in which the user can delete and add tags, as well as deleting files.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/editdoc.png)

### Social Media Search
The Social Media Tracker page has two options, Reddit and Twitter. Click either one and you are presented with a search bar. Enter your term search term. Returned are posts and discussions related to the query. The following example is a Twitter search, but reddit looks almost identical.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/TwitterSearch.png)
You then have the option to go directly to the Tweet, or recommend documents that are relevant to the dicussion.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/DocRec.png)

### Users
The Admin can also add and delete users through the Users menu.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/Users.png)
Click on a user and you can see their details as well as the option to delete the user.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/UserXander.png)
You can also add more users, should any new members join the group.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHHCapsPics/master/docs/DocPics/CreateUser.png)
