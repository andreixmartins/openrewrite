


# Openrewrite 

Openrewrite is an automated refactoring tool that applies declarative “recipes” to safely update code and build files at scale. 
Use it to upgrade libs, fix APIs, enforce dependency rules, and clean up.

Check the rewrite.yml file that contains all recipes used in this repo. Also, take a look in the pom.xml to understand how operewriter plugin works.

Run this maven command mvn rewrite:run  to apply all recipes declared in the rewrite.yml file, after that check the differences in your pom.xml


## Extra Openrewriter Maven commands

- Dry-run command
```bash
mvn -Drewrite.dryRun=true rewrite:run
```

- Force config location 
```bash
mvn -Drewrite.configLocation=/abs/path/rewrite.yml rewrite:run
```

- How to run dynamically recipes
```bash
mvn -Drewrite.configLocation="$(pwd)/rewrite.yml" -Drewrite.activeRecipes="com.amartins.RemoveOldStruts" rewrite:run
```



