$ ./tree-md .
# Liquibase

Change Log Example:
...
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<databaseChangeLog
        xmlns="http://www.liquibase.org/xml/ns/dbchangelog"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://www.liquibase.org/xml/ns/dbchangelog
                      http://www.liquibase.org/xml/ns/dbchangelog/dbchangelog-3.5.xsd"
        logicalFilePath="src/main/resources/liquibase/changelog/install.xml">

    <include file="src/main/resources/liquibase/changelog/cleanUpLiquibase.xml"/>

    <includeAll path="src/main/resources/liquibase/changelog/install/seq" />
    <include file="src/main/resources/liquibase/changelog/install/table/master.xml" />
    <includeAll path="src/main/resources/liquibase/changelog/install/cst" />
    <includeAll path="src/main/resources/liquibase/changelog/install/trigger" />
    <includeAll path="src/main/resources/liquibase/changelog/install/pks" />
    <includeAll path="src/main/resources/liquibase/changelog/install/pkb" />
    <includeAll path="src/main/resources/liquibase/changelog/install/functions" />

    <include file="src/main/resources/liquibase/changelog/install/data/reference_data.xml" />
    <include file="src/main/resources/liquibase/changelog/v0.0.0.0/master.xml" />
    <!-- <include file="src/main/resources/liquibase/changelog/2016-08-22/master.xml"/> -->

    <changeSet author="MajorVersion" id="0.0.0.0" />

    <include file="src/main/resources/liquibase/changelog/v1.0.0.19/master.xml"/>
    <include file="src/main/resources/liquibase/changelog/2016-08-30/master.xml"/>

</databaseChangeLog>
...


Directory structure:
```
.
 * [tree-md](./tree-md)
 * [dir2](./dir2)
   * [file21.ext](./dir2/file21.ext)
   * [file22.ext](./dir2/file22.ext)
   * [file23.ext](./dir2/file23.ext)
 * [dir1](./dir1)
   * [file11.ext](./dir1/file11.ext)
   * [file12.ext](./dir1/file12.ext)
 * [file_in_root.ext](./file_in_root.ext)
 * [README.md](./README.md)
 * [dir3](./dir3)