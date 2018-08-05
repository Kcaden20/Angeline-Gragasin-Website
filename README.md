# Angeline Gragasin Personal Website 

This README is the documentation for Angeline Gragasin's website. It was developed between the summer of 2017 and 2018. It was built using HTML, CSS3, PHP, Bootstrap, jQuery. It uses Kirby Flat-File 2.5.6 for content-management and Flickity 2 for the slideshow animations. The IDE used for this project was Coda 2.6.10

## Getting Started
The site is structured using Kirby Flat-FIle CMS which uses folders to create an architecture to access. None of the folder names should be changed for any reason, nor should they be deleted, nor should the folders within them be renamed or deleted either. Only the following folders have editable files but still should never be renamed: 

```
Content > Page > Project.txt 
Assets > [JS, CSS, FONTS, FAVICONS, IMG] > Files 
Site > [FOLDERS] > PHP Files 

```

All other folders should be left alone. Within these three editable folders, the one that will be changed frequently is the Content Folder. 

The Assets Folder in case of any changes needing to be made to visual or interactive aspects of the site itself and finally the Site folder in case of any restructing of the content architecture. The Site Folder should not be editted without knowledge of how Kirby's PHP and YML (contained within the Blueprint Folder) works. Finally, with editting these last two, they should be editting initially on a local version of the website before being kicked up the live version. 


## Editing Content 
Kirby Flat-File CMS works by structing content into folders and then having php templates access that content stored in the folders. There are two ways to edit the content in Kirbys CMS. 

1. Through direct manipulation of folders and files
2. Through the Kirby Panel 

Generally, using the first option is discouraged as it can cause issues if errors are made while editting the content or anything is accidentally deleted. It should be used as a last resort if  some kind of issue is happening with the panel. How you access content in this way is through 


### Content Editting Through Direct Manipulation 

```
Root Directory > Content > Page > Subpage (If applicable, some pages do not have subpages)
```

In the final page of the tree, you will see the following 

```
project.txt 
any other content that has been uploaded
```

The project.txt file is integral as in here is where you fill out all the categories you've allowed in your blueprint, including text, images, embedding videos and all else. Prior to the creation of the panel, this was the main way of editting content on kirby and the lack of a visual interface made it difficult to edit between looking at the blueprint and txt file. 

Once opening project.txt, you still see the different categories of content available followed by their accompanying text or images. Note that there may be more categories here that do not show up on the panel. This may because categories were added or removed from Kirby's Panel but are still present in this txt file as the panel does not clear out extraneous categories from earlier versions of the site. Editting these does nothing and they are better left alone for the sake of preserving the structure of the txt file. Once finished editting the txt file, just save it. For the changes to take hold. 


### Content Editting Through The Panel

To access the panel for the website, type in the following: 

```
https://www.angelinegragasin.com/panel/
```

From here, you will be asked for credentials. After entering them in, the Dashboard will show up giving options to navigate the site.  

### Hamburger Bar
At the top left, there is a hamburger menu, when clicking on it, the following options will drop down. 

```
Dashboard
Site Options
Users 
Logout
```

### Site Options
This page wil give you information about your kirby license, and give global editable fields around the title of the site, what is in the footer, a meta description for Google as well as the files for the cursors.


### Users 
Here, you will see all the accounts that have been made and that can edit this website. As an admin, you have control over all the accounts and can give other users their specified roles. This is between Admin (control over all aspects of the site) and Editor (can only edit and access content)

For more information on Kirby Users please access the Kirby Documents around [Users](https://getkirby.com/docs/panel/users)

### Your Account
Clicking edit will allow you to edit aspects of your account, changing passwords, adding names and changing your role. 

### Pages
Most of your time and energy will go into editing the Pages tab of the website. It is not recommended to add more top-level pages as it could mess up the navigation of the site. Within Pages, the page spent the most time editing will be the Archive. Here will be where you add projects, update content and add images. 

    Pages are by default made invisble, they can be previewed and are issued a template to follow upon creation. The template used entirely at this point will be the "Cases" template with writing being from an outdated version of the site. 

If you need to learn more about all the options available within Kirby Text, there is a 101 File embedded into the site and can be accessed [Here] (http://www.angelinegragasin.com/assets/docs/kirbytext101.html)

### Resource
For more on the Panel, visit the [Kirby Doc] (https://getkirby.com/docs/panel)

## Editing Assets 
While this folder will very rarely be edited, I'm sure there may be small tweaks you want to make. 

### Editing CSS
To edit the CSS, go to the following

``` 
Assets > CSS 
```

In here the main file you may edit will be the main.css. There are about 7,000 lines of code here so opening it up can be very daunting. Having a web inspector open, looking at what line what you want to edit is on and then finding that line in your IDE is the most efficient way to make changes. Some changes such as color or font however, can be more difficult to make with many elements using these. 


### Editing Javascript 
Editing the Javascript is more rare than the CSS. While CSS will be the Assets folder, the JS used for this site is NOT in the Assets folder. It is actually found here: 


``` 
Site > Snippets > Footer.PHP
```

Within here, you'll find a script tag with all the Javascript & jQuery used for the site. 


## Editing the Site

Editing the Site Folder is not recommended to be done without a strong knowledge of the Kirby API. Within the Site Folder, there will be a lot of subfolders, the main ones to edit will be:

```
Blueprints
Templates
Snippets, 

```
These three work in conjunction with one another. Blueprints is where you add what fields you want in your panel. However, adding a new field in the blueprint and then filling it with content will not make your new content appear. The new field then needs to be declared within the Template. After linking these two is when the new content will appear on the pages. Snippets are bits of code that reoccur throughout the site, so things such as the footer or header can be made into snippets thus reducing the amount of code on each page.  

### Templates & Snippets 
Editting these is too big of a topic to cover in this readme.md. To learn more about these two please visit [here](https://getkirby.com/docs/templates)

### Blueprints 
Editting Blueprints will be done not in PHP but in YML. This coding language has no tags and takes spaces, indentations and title case very importantly. To learn more about blueprints visit the [Documentation] (https://getkirby.com/docs/panel/blueprints)

### Resources 
For more on editting the Site templates visit [here] (https://getkirby.com/docs/cheatsheet)
For more information on PHP and learning PHP, vist the [PHP Website] (http://php.net/manual/en/tutorial.php)



## Running a Local Version of the Site 

Any changes to the Site or Assets Folder content should be made on a local version of the site before changing it on the live version. In order to run the local version, I will be sending a final developmental version via WeTransfer. This folder should be placed within the MAMP Application in the HTDOCS folder. Once in here, then open up terminal.

```
cd where-the-folder-is-located
```

After using cd to locate the folder, all you have to type into your terminal is 

```
gulp 
```

This should run a local version of the site on your computer. From here, the same rules for edittable folders still apply. The developmental version has a couple of extra other files that are needed when running locally but do not need to uploaded onto the server. After you've finished editting the files and are happy with the changes, change out those files within the server. 


## Support 

* Having made the site, contacting Kevin Cadena would be a good option to reach out to regarding changes to the site and can be reached at hello@kevincadena.com 

* Besides Kevin, there is also a forum specifically for Kirby that is staffed with admins and helpers whose job is to answer questions about devleopment. [Link](https://forum.getkirby.com/)



## Built With

* [Kirby](http://getkirby.com/) - Content Management
* [Kirby Bootstrap Starterkit](https://github.com/Lassedupont/kirby-bootstrap-starterkit) - Web Framework Used
* [Flickity](https://flickity.metafizzy.co/options.html) - Used for the complex slider 


## Authors

* **Angeline Gragasin** - *Owner, Direction & Content* - [Portfolio](http://angelinegragasin.com/)
* **Kevin Cadena** - *Design & Development* - [Portfolio](http://kevincadena.com/)



## Acknowledgments

* Thanks to Kirby for the amazing CMS
* Metafizzy for making the best slider possible
* Hendrik Berends who ported Bootstrap to Kirby! 
* The Kirby Forums for having such dedicated and knowledgable regulars who helped me on countless issues with the site. 

