20211114

1400 download visual Studio 2022 and .net6.0, and installed them

1600 tried to open my project with VS2022 and built it, succeeded.

1623 tried to add Micriosoft.EntityFrameworkCore.Relational, failed! it said as2(the first project
I created is not compatible with .net6.0)

1650 created new projects called test, still not worked.

1820 created a brand new project ZhijunsBooks,start over assignment 2.

1825 noticed that the vs2022 has merged startup.cs and program.cs, find the services.adddefaultidentity
<identityUser>(....), which (has builder before service) is different with the slide 7.
--but i tried to delete the parameter anyway
--built the project.
--worked normally

1831
--replace existing bootstrap.css to darkley bootstrap.css by copy and paste codes
--replace site.css with site.css provided by teacher
--modify file name from bootstrap.min.css to bootstrap.css in shared/_layout.cshtml--href
--modify text style of navbar, footer, and loginpartial
--built, succeeded, and style was applied.

1903 part 1.4
--add three more projects
--copy data file from zhijunsbooks to zhijunsbooks.dataaccess
--switch to zhijunsbooks.dataaccess, install microsoft.entityframework.core.ralational and sqlserver, succeeded

1923
--check the dependency/packages, find that sql and relational package were added to zhijunsbooks instead of 
zhijunsbooks.dataaccess.
--started over until before adding EFCore

2155
--found out that in the console, there is a default project menu, switch to the desired
project, then run Install-Package Microsoft.EntityFrameworkCore.relational, everything went
well
2156
--open my projects
--delete data folder in the ZhijunsBooks.DataAcess and copy the file to ZhijunsBooks.DataAcess 
--choose my current project in the top menu and open package manager console, switch 
default project to ZhijunsBooks.DataAcess
--run Install-Package Microsoft.EntityFrameworkCore.relational
--succeeded, check project ZhijunsBooks.DataAcess, there is additional file added in the dependency
/packages with relational ended.recorded the six files in packages
--run Install-Package Microsoft.EntityFrameworkCore.SqlServer
--succeeded, but i dont see any changes, actually sqlserver already there before running
both commands.
--deleted migration folder in Data folder, save the four projects as version 2
--run Install-Package Microsoft.identity.EntityFrameworkCore, succeeded
--check packages, identity.entityframeworkcore(1.2.7) was added in the project .DataAcess
--change the namespace in file Data/ApplicationDbContext.cs, but it showes error says
both identity.EntityFrameworkCore and microsoft.AspNetCore.EntityFrameworkCore have it.
--delete identity.EntityFrameworkCore file, error gone.

2228
--tried find file Class1.cs, but not found yet
--built the project .DataAccess, succeeded

2247 work on page 34
--Move Models in to BooksInbulk.Models, but can not find BookInBulk
--rename Models in ZhijunsBooks.Models to ViewModels
--modify errowViewModels.cs, namespace to namespace ZhijunsBooks.Models.ViewModels in
ZhijunsBooks.Models.
--add project reference to .DataAccess and .Model projects