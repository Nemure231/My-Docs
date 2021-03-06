## Documentation

This documentation is for Developer only, who have understanding basic static website. But if you are not a Developer and still want to manage this code alone by yourself, please read this documentation carefully.


## Introduction

Tailwindcss is CSS fremework that i installed through npm (Node Package Manager), npm is a site or a tools that provides package publications for CSS and Javascript, packages is a well-made code function that already finished, so we can use that instantly in our project. The base concept of npm is like Goggle Play Store, someone publish their package in npm and some people can install the package to use it in their code. The problem is when the version of the package Tailwindcss is updated you always need the latest version of it right?

## Install Code Editor

If you are not a Developer, you will need Code Editor App, because you need to open your own code. If you have low/mid-tier laptop/computer i sugess you to install Sublime Text 3 as your Code Editor, because that the lightweight app i ever use. And if you have high-tier laptop/computer just install Visual Studio Code, that is the most feature-rich code editor.


[Sublime Text 3](https://www.sublimetext.com/3)

[Visual Studio Code](https://code.visualstudio.com/ )


## Installing npm and NodeJs

Npm is not a tools that can work in independently, npm need NodeJs for their base program language to make it works. So please follow the instruction below:

1. Visit [NodeJs Website](https://nodejs.org/en/download/)
2. Choose the version based on:
   - Your system operation, 
   - Your bit processors,
   - Choose the LTS version it's a stable version,
   - Choose the .msi extension,
3. After you downloaded it, time to install:
   - Click the NodeJs installer file
   - System will ask if you want to run the software, click Run.
   - You will be welcomed to the Node.js Setup Wizard, click Next.
   
   ![This is an image](https://blogs.masterweb.com/files/2020/05/Wizard.jpg)
   
   - On the next screen, checked the license agreement, and click Next.
   
    ![This is an image](https://blogs.masterweb.com/files/2020/05/Accept-terms.jpg)
    
   - The installer will prompt you for the installation location. Leave the default location, unless you have a specific location to install it somewhere else, then click Next.
   
    ![This is an image](https://blogs.masterweb.com/files/2020/05/Destination-folder.jpg)
   
   - The wizard will let you select custom service, we just need Node.js runtime, npm, then click Next.
   
    ![This is an image](https://blogs.masterweb.com/files/2020/05/Custom-setup.jpg)
    
   - Finally, click the Install button to run the installer. When it finishes, click Finish.
   
   ![This is an image](https://blogs.masterweb.com/files/2020/05/Install.jpg)
   
4. Always check if the NodeJs and npm already installed or not
   - Open your Command Prompt
   - Type `node -v`, then click Enter, if you see node js version its already installed
   - Type `npm -v`, then click Enter, if you see node js version its already installed
  
   ![This is an image](https://blogs.masterweb.com/files/2020/05/Cek-versi-node-js-dan-npm.jpg)
  
5. To updating this software you just need to download the latest version and install it again, your system will replace the version again.


It's super easy to update your Tailwindcss version just with small npm command, however we also need to update production Tailwindcss with the new one, and update minify-css. **Remember always turn on your internet when you follow this guide**, we need a connection when doing all of this stuff. This is the small roadmap to update Tailwind css:
1. Updating Base Tailwindcss
2. Updating Production Tailwindcss
3. Updating Minify Tailwindcss


## Updating Base Tailwindcss

What are we going to do is updating the base code of Tailwindcss. Because the production css and the base of Tailwindcss source is different file.

1. Open your project folder with File Explorer.
2. If you noticed, there is a file named "package.json", if the file is exists, then you are in the right location.

![Screenshot_2022-01-19_13-50-04](https://user-images.githubusercontent.com/49015080/150078990-6e503825-ff4b-4614-965b-6a5a4f491084.png)

4. Open the package.json with your Sublime Text 3/Visual Studio Code
5. In that package.json you will see the version of Tailwindcss, in the "devDependencies" line.

![Screenshot_2022-01-17_22-36-12](https://user-images.githubusercontent.com/49015080/149798816-d411a43e-1cba-410c-a581-6e79e7ad3bcd.png)

6. Compare your Tailwindcss version with the current version on their [website](https://tailwindcss.com/docs/installation), you can see the version on the navbar

![llll](https://user-images.githubusercontent.com/49015080/149788965-8437e7da-e236-4253-a6e1-d10eedff71f9.png)

7. If your version is smaller, then you need to update.
8. Open your Command Prompt on your root project location, the same location where "package.json" exist.
9. Type `npm update`
10. The loading progress will apper on your Command Prompt, wait until is finish.
11. And finally, you just updated your Base Tailwindcss.
   
   
## Updating Production Tailwindcss

The Base Tailwindcss have a fully class function, even a class that we don't need to use, what a waste right? But with creating the Production Tailwindcss, we just get what we need to use, for example there is a 1000 class on Base Tailwindcss, but we just need 70 class function out of 1000 class. So we can remove unnecessary class and change it form 70/1000 class to only 70/70 class, and make the size is more smaller to load in the website.
   
You need to update your Production Tailwindcss not only because there's a newers version of Base Tailwindcss, but everytime you changed/modified your index.html file, you need to update the production file. For example you need to use class "font-bold" to give your text bold effect, but in the Production Tailwindcss, there's no class called "font-bold" we can't use that class, because in the previous work, I (as a Developer) didn't need a bold effect on the website, remember what i said: 

> We just get what we need to use 

Before that i don't need "font-bold" but i need it now. How can i get the "font-bold" class in Production Tailwindcss? **I can get it in Base Tailwindcss. In Base Tailwindcss, they have all of the class, including "font-bold". So all we need to do is get the "font-bold" in Base Tailwindcss and put it into Production Tailwindcss.**

Actually this method is called "Watch" more than "Update", so the Tailwindcss can "Watch" our HTML file and scan them, and if there's a new class, Production Tailwindcss will get that class in Base Tailwindcss and add that class automatically.
![Screenshot_2022-01-19_14-14-49](https://user-images.githubusercontent.com/49015080/150082212-f2dab306-d7a3-4e99-9b11-b3cc58fcf35a.png)



That's it's. Lets get started how to update/watch:
   
1. Open your project location, and go to this location your_project/public/assets/base/tailwindcss
2. You will see the "input.css" and "output.css", the input file is our base Tailwindcss that already updated before, and output will be our production file

![Screenshot_2022-01-19_14-17-28](https://user-images.githubusercontent.com/49015080/150082612-bbb119b5-2a50-4a11-b3b6-d956a927c3ee.png)

3. Go back again to root of your project location
4. You will see there is a file named "tailwind.config.js" that the setting file we needed for making production Tailwindcss
5. Open that file with your Sublime Text 3/Visual Studio Code

![Scssd](https://user-images.githubusercontent.com/49015080/149789339-28335ffa-f5d7-4439-9c7b-45da5778de37.png)

6. Take a look at `["./public/**/*.html"]`, that is your HTML file location, this fuction code `**/*.html` is going to find any HTML file in your public folder so don't remove it. Public folder is the base location i always used to store my HTML file, if you change or move the HTML file, you need to change the location based on your own index.html location, for example if you move it on `/public/my_page/` just change to `["./public/my_page/**/*.html"]`
7. Close your tailwind.config.js if your HTML file in the right location
8. Open Command Prompt and type `npx tailwindcss -i ./public/assets/base/tailwindcss/input.css -o ./public/assets/base/tailwindcss/output.css --watch` The first location is your input location and the second is your output.

![Screenshot_2022-01-17_21-40-32](https://user-images.githubusercontent.com/49015080/149789802-4e0d68ba-e265-45ff-ad17-8db73572a52c.png)

9. After that. just click enter and now your Tailwindcss is begin to do the watch process
   
### Note:
Remember, keep the watch process turn on when you activated it, don't close your Command Prompt when your Tailwindcss in watch mode. But why it's must always on? Because the Developer always need to get the new class when they are create the website. Everytime you add/remove class in your index.html and save it again, Tailwindcss will add/remove your class in Production Tailwindcss.

If you stil can't figure my explanation, watch this video below:

https://user-images.githubusercontent.com/49015080/150089166-124361fb-d5a6-4dc8-b640-2d0f5012e13c.mp4


### Tips:
Do you think the syntax for watch Tailwindcss is too long? Actually you can short it. If you open your "package.json" file, you will noticed in the "scripts" line 

![Screenshot_2022-01-17_22-22-38](https://user-images.githubusercontent.com/49015080/149796832-037ec7a3-f8bd-4aa8-ab32-3bee7ad883fd.png)

There's a same syntax but warped with `"tailwind-watch": "npx tailwindcss -i ./public/assets/base/tailwindcss/input.css -o ./public/assets/base/tailwindcss/output.css --watch"`. If you type `npm run tailwindcss-watch` in Command Prompt, Tailwindcss will run the watch process. Because i am alreay made my own npm function that called "tailwindcss-watch" the inside of that function is the long Tailwindcss watch syntax.

https://user-images.githubusercontent.com/49015080/150089553-c8c467e8-87eb-4e2b-bca0-5d5b4c453229.mp4



## Updating Minify Tailwindcss
   
After you are done with Production Tailwindcss and you don't need to change the HTML file anymore, your final result of Production Tailwind is stored in output.css. Now, all you need to do is updating your minify-css, because the minify-css is based on Production Tailwind, if you change it, then you need to update your minify-css also.

The Minify CSS is smaller version of CSS file, this is the best type of CSS if you want to put in the production use in my opinion. Production css is better but minify-css is more better. The main different from normal CSS is the extension name, Minify CSS have extension name ".min.css" There's a lot of website in the internet can minify your css like this [website](https://www.toptal.com/developers/cssminifier/) yoU can use their service, or you can do it with a few npm command again? Let's do it.

1. Go open your "package.json" file in your root of project
2. You will found "minify-css" in the script line, the first location of that script is your "output.css" and the second is your "output.min.css"

![mop](https://user-images.githubusercontent.com/49015080/150090201-90629f31-f2aa-4c24-ac1c-c9c716b17739.png)

3. If you already have "output.min.css" in your `your_project/public/assets/base/tailwindcss`, it will be replaced. if you don't have, it will be added on that folder.
4. Open your Command Prompt in the root of project
5. Type `npm run minify-css`
6. Wait until the loading finish
7. And done  


## Super Quick Update

Sorry for long guide, i just want you know about the basic. If you already know the basic that i explain above, you can do this quick update:

1. Open your Command Prompt in your root of project
2. Type `npm update`, then click Enter, to update Base Tailwindcss, wait until finish
3. Type `npm run tailwindcss-watch`, then click Enter, to update Production Tailwindcss, wait until finish
4. Stop the watch process, just hit `CTRL + C` in Command Prompt
5. Type `npm run minify-css`, then click Enter, to update Minify Tailwindcss, wait until finish
6. Done, quick right?


## Updating Alpinejs

Alpine my favorite Javascript Framework, if you find Alpinejs in my code, of course you need to update it if you want. But mostly, i use Alpinejs because i need complex Javascript case. Let's get started:

1. Open your project location
2. Open public/assets/base
3. If you find alpinejs folder you need to continue this guide, if you don't then you good go close your project
4. When you open the alpinejs folder you will see alpine.min.js
5. Open that file with Sublime Text 3/Visual Studio Code, take a look at the version your Alpinejs version

![Screenshot_2022-01-17_23-23-33](https://user-images.githubusercontent.com/49015080/149806029-96ab94f1-6d1d-4491-a7c8-8ab78e50e285.png)

7. Open [Alpinejs website](https://alpinejs.dev/essentials/installation) to see the latest version

![mlmlmlm](https://user-images.githubusercontent.com/49015080/149805154-04ad0b48-2443-4211-83b0-ad31a50e4f6d.png)

8. Compare both version file, if your version is smaller, then you need to update.
9. Open again your alpine js file with Sublime Text 3/Visual Studio Code in your_project/public/assets/base/alpinejs
10. Find "alpine.min.js" file
11. Open it
12. Delete all of the old code
13. Open their latest link version https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js or you can see in [Alpinejs website](https://alpinejs.dev/essentials/installation)

![dmdmm](https://user-images.githubusercontent.com/49015080/149806484-3ff6cd04-34c1-40d3-b5ef-c76e7ad9e252.png)

15. Copy all of that code in that website
16. Paste it in your alpine.min.js 
17. Done
