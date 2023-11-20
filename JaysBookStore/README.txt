2023-10-24

1502
Created a new project with authentication to be individual accounts and tested the application.
1505
Added the README.md file and edit the content of it.
1510
Relaunch the project and added the test registeration account with email id j@j.com.
1525
Drop the whole project and restarted because forgot to enable the razor runtime compilation and go through whole once again and this time it is making changes (./Views/Shared/_Layout.cshtml).

2023-10-27

1432
resumed from where i left.
1437
Selected the Bootstrap theme and downloaded the Bootstrap file.
1440
Replaced the Existing Bootstrap file in wwwroot>lib>bootstrap>dist>css>bootstrap.css and also changed the name of the old css file to "bootstrap_old.css".
1443
Donwload the site.css file from the given file and replaced the existing file wwwroot>css>site.css.
1450
In _Layout.cshtml change the file name from bootstrap.min.css to bootstrap.css as given in the ppt.
1452
Changed the nav class from nav-light to nav-dark and also the bg-white to bg-light.
1455
On line 23 removed the text-dark and all added the some additional properties to footer class.
1500
Removed all the 'text-dark' in _LoginPartial.cshtml and run the project.
1510
Added the Additional stylesheet and scripts link which are given in CSS_JS.txt file in the file folder on blackboard.
1523
Added the Dropdown code 
"<li class="nav-item dropdown">
                            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button">
                                Content Management
                            </a>
                            <div class="dropdown-menu" area-labelledby="navbarDropdown">
                                <a class="dropdown-item" href="#">Action</a>
                                <a class="dropdown-item" href="#">Another Action</a>
                                <div class="dropdown-divider"></div>
                                <a class="dropdown-item" href="#">Something else here</a>
                                </div>
</li>". But ran into problem that when i clicked on the Content management it didn't open the drop down menu
1546
Tried to solve it but didn't find the solution and give up push all the changes to github.

2023-10-31

1023
Cloned the project and try to re-run it but giving me error of localhost {port} doesn't avaiable.
1025
Dropped the whole project and tried again.
1111
Reached at the same point.
1118
Started creating all three project as follows - BookApp.DataAccess, BookApp.Models and BookApp.Utility
1121
Moved the data folder from main to DataAccess folder
1123
Deleted the Migration folder in data folder and install Microsoft.EntityFramework.Relational and sql server from Nuget Package manager.
1125
Modified the namespace in ApplicationDbContext.cs and deleted all Class1.cs in new project.
1127
Moved the Models folder to Models project and add project reference to .DataAccess and .Models 
1129
Renamed the models folder to ViewModels and Build the project but gave me error in Startup.cs 
1131
There was error ApplicationDbContext on line 37, hover on the error and clicked on lightbulb and added this - using BookAppNew.DataAccess.Data; and removed using data line;
1134
Correct the default reference of Error.cshtml and new one is BookAppNew.Models.ViewModels.ErrorViewModel and try run the project but again an error
1136 
Error was in HomeController.cs where type or namespace for error model not found, did the same thing hover and clicked on bulb and added - using BookAppNew.Models.ViewModels;
1139
Added new SD.cs class in Utility  and modify the class property
1140
Added the project reference
1142
Added "Customer" area in Area folder and changed the startup.cs route -  pattern: "{area=Customer}/{controller=Home}/{action=Index}/{id?}");
1145
Edited the HomeController.cs to explicitly define that the controller is in the Customer Area
1147
Moved Views > Home and modify the HomeController namespace
1149
Copied _ViewImport and _ViewStart to Customer Area and added new path -  Layout = "~/Views/Shared/_Layout.cshtml";
1151
Added the proper view files like above folder and delete the Data and Models folder
1152
commit all the code to github
1155
Forgot to delete the controller folder delete it and comment the - options => options.SignIn.RequireConfirmedAccount = true on line 35 and commit it 

2023-11-06
1953
Cloned the project and changed the project appsetting.json = "Server=(localdb)\\mssqllocaldb;Database=BookAppNew;Trusted_Connection=True;MultipleActiveResultSets=true"
1956
add the first migration - 20231107005626_AddDefaultIdentify
2001
added second migration - 20231107010052_AddCategoryToDb but it was empty 
2003
the migration where all the things added - 20231107010259_updatedMigration
2007
Created new folder Repository and IRepository and created interface and class file
2011
Created new class and interface file as categoryRepository 
2014
Created ISP_Call.cs and installed the Dapper package and push to git hub
2017
Created new UnitOfWork and its interface file 
2019
 services.AddScoped<IUnitOfWork, UnitOfWork>(); this to startup.cs
 2024
 added the new CategoryController.cs in area admin folder and modified the code according to slide
 2027
 Created new Index.cshtml file and added code that you provided
 2030
 Added the drop down and javascript file from the BlackBoard
 2034
 Created new upsert.cshtml and modified the code according to the blackborad code.
 2036
 Added both partial view named _EditAndBackToListButton and _CreateAndBackToListButton
 2040
 Added the asp-action to the Index.cshtml page and ran the application
 2042
 Modified CategoryController.cs
 2044
 Added the Delete functions in category.js and run the application

 2023-11-20
 1750
 Restarted the whole project with new name - JaysBookStore and the first migration of part 2 - 20231120225015_AddDefaultIdentityMigration

 1755
 Added the second migration - 20231120225444_addCategory

 1757
 Added the third migration - 20231120225735_AddedNewCategory

 1841
 Created New model CoverType.cs 
 1846
 Created new class and interface for coverTypeRepository and added the migration - 20231120234643_CoverTypeDb