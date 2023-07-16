# Notes

``` txt

dotnet new sln
dotnet new console -o zscon -f "netcoreapp3.1"
dotnet new classlib -o zslib -f "netcoreapp3.1"
dotnet new xunit -o tests/zsxunit.tests -f "netcoreapp3.1"
dotnet new specflowproject -o tests/zsspecflow.tests -f "netcoreapp3.1" -t xunit
dotnet new specflowproject -o tests/zsplaywright.tests -f "netcoreapp3.1" -t xunit
dotnet sln add zscon/zscon.csproj
dotnet sln add zslib/zslib.csproj
dotnet sln add tests/zsxunit.tests/zsxunit.tests.csproj
dotnet sln add tests/zsspecflow.tests/zsspecflow.tests.csproj
dotnet sln add tests/zsplaywright.tests/zsplaywright.tests.csproj
dotnet add zscon/zscon.csproj reference zslib/zslib.csproj
dotnet add tests/zsxunit.tests/zsxunit.tests.csproj reference zslib/zslib.csproj
dotnet add tests/zsspecflow.tests/zsspecflow.tests.csproj reference zslib/zslib.csproj
dotnet add tests/zsplaywright.tests/zsplaywright.tests.csproj reference zslib/zslib.csproj
dotnet add tests/zsplaywright.tests/zsplaywright.tests.csproj package Microsoft.Playwright

```