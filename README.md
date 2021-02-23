# Kentico Gitignore

This gitignore file is designed to help you ignore/include all the right files in your Git repository for Kentico projects. 

## Important notes
1. Uses the default ignore from Visual Studio as the starting point.
1. Tested in **Kentico 9** only. 
1. **Ignores** the `bin` directory and **includes** the `Lib` directory.
    * You can restore the Kentico DLLs from the `Lib` directory after restoring a repository for the first time.
1. **Ignores** starter site files.

More information at http://devnet.kentico.com/articles/gitignore-for-kentico

## Protecting sensitive settings
Even if your repository is only intended for private distribution you should avoid allowing sensitive and/or environment specific data such as connection string and hash string salts from being checked into your source control. rather than ignore the whole `web.config` file, we recommend adding `file="AppSettings.config"` and `configSource="ConnectionStrings.config"` to the app settings and connection strings elements in the `web.config` respectively. Next, move the sensitive data to those files. It is also recommended that you also add template versions of these files for reference. When pulling a fresh copy of the repository the developer should request a copy of any sensitive data from another developer or some other secured location. You can find an example of this practice in the [Kentico MVC sample site on GitHub](https://github.com/Kentico/Mvc/tree/master/src/DancingGoat).

