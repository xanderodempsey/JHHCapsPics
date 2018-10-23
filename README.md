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
    cd JHH_Capstone/code/judd && npm install
    ```

5. Open MySQL Workbench and enter the Local instance MySQL router.

6. Right click under Schemas > Create Schemas
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/CreateSchema.png?token=AULzRUiYOhGEuNj7EGnM9KfkkZ_CA2a-ks5bypmzwA%3D%3D)

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
cd JHH_Capstone/code/judd && nodemon index.js
```
and in your browser of choice goto localhost:3000

### Public Site
The first thing you seen once link is opened you will be presented with the home page.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/Homepage.png?token=AULzRa4JJxT0cysDM5gBRASFXzl3nCg0ks5byqQbwA%3D%3D)
From here, a general vistor to the site can access the documents hosted as well as searching for documents by tag.

The following picture is what a user will see once accessing a document (this example is a journal article, and because of copyright issues cannot be hosted physically on the site. So a DOI is given instead.)
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/Document.png?token=AULzRSt3A_roGv6_bWXBL37Mf3ik7KSQks5byqYzwA%3D%3D)

### Admin Login

To access the other features of the site requires an Admin login, this can be done by accessing the link at the bottom of the site. Once clicked,you will be redirected to the following page.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/adminlog.png?token=AULzRdq0h8oXHQGk-KHDoG2zTUoMlhLHks5byqbcwA%3D%3D)

Once logged in, you will get redirected to the same page. Although the user now has access to the Admin Features: Upload, File Manager, Social Media Tracker, Users.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/adminhome.png?token=AULzRYtT1WrMOR-_gXkoKpq8-xA_VPoiks5byqfswA%3D%3D)

### Uploading Files
Click on the Upload option in the top menu. This redirects to two options: upload a File, or Link a Document.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/UploadOptions.png?token=AULzRZs04qhDUT1nnd7MG1Zip2EyQowoks5byqiVwA%3D%3D)

In the file upload, the user needs to choose a file from their directory, add a display name that the end user will see, and as many tags as you wish.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/uploadfile.png?token=AULzRW5xS6ldEyEcLwGvepGIh3MGzCChks5byql1wA%3D%3D)

Similar to uploading files, to link a document you simply need to add the link in the text field, then follow the same procedure. *Please note that for a URL you must proceed the link with https:// and for a DOI https://doi.org/*
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/uploadlink.png?token=AULzRUu9Zkz1xdAaGsSzeZiq3zbfgccbks5byqsJwA%3D%3D)

### Managing Files
The File Manager tab looks identical to the Document menu, except now when you access the documents you get taken to a page in which the user can delete and add tags, as well as deleting files.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/editdoc.png?token=AULzRaX73jW2wdnAcckGXHOutRpIiyvZks5byrUbwA%3D%3D)

### Social Media Search
The Social Media Tracker page has two options, Reddit and Twitter. Click either one and you are presented with a search bar. Enter your term search term. Returned are posts and discussions related to the query. The following example is a Twitter search, but reddit looks almost identical.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/TwitterSearch.png?token=AULzRRtALSj9BSqNYX470tCslvkBFAtxks5byrfAwA%3D%3D)
You then have the option to go directly to the Tweet, or recommend documents that are relevant to the dicussion.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/DocRec.png?token=AULzRZVnNGzHsudE9DRJq5jBBCZHw3odks5byrhCwA%3D%3D)

### Users
The Admin can also add and delete users through the Users menu.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/Users.png?token=AULzRdwTOXQAGfq9cUFT2Zg1U5-dE4Ipks5byrjHwA%3D%3D)
Click on a user and you can see their details as well as the option to delete the user.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/UserXander.png?token=AULzRVWkF6qYqNlmg5nlwMnatPLRDi1Jks5byrk_wA%3D%3D)
You can also add more users, should any new members join the group.
![alt text](https://raw.githubusercontent.com/xanderodempsey/JHH_Capstone/master/docs/DocPics/CreateUser.png?token=AULzRd1iQmiFLhyKCEutMP2oCvYLNMBnks5byroAwA%3D%3D)
