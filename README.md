# ASP.NET Core Upload big files
Uploading files in ASP.NET core is largely the same as standard full framework MVC, with the large exception being how you can now stream large files. We will go over both methods of uploading a file in ASP.NET core.

I wrote a post [Uploading files in ASPNET Core](https://www.puresourcecode.com/dotnet/net-core/uploading-files-in-aspnet-core/) on [PureSourceCode](https://www.puresourcecode.com/) to explain in detail the code.

## Implementation for .NET Core 2.x and 3.x
When you run the app, you have the following screen to try different scenarios.
![image](https://user-images.githubusercontent.com/9497415/150338469-8ef38299-7c86-4b93-930b-dd45480b94c6.png)

## Implementation for .NET 5.x or above
The first implementation is for uploading large files reasding the content from the `Request`. To use this version, you have to use Postman or CURL.
![Call the API with Postman](https://user-images.githubusercontent.com/9497415/150338216-4a3d32be-09d4-45b5-9a28-283e3f26395f.png)

In the second implementation, the file is passed as `IFormFile`. To upload the file from Swagger, we have to add a proper filter `SwaggerFileOperationFilter`.
![Change Swagger to upload file](https://user-images.githubusercontent.com/9497415/150338234-0b91bc6c-7aa4-4bb0-8689-090c7a2def73.png)
