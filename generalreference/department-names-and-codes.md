# Department Names and Codes

## Definition

The City and County of San Francisco is made up of many organizations that perform work and deliver services according to the charter and administrative codes of the City. 

These organizations have common names, but also codes that are used in accounting for the work and services performed. The [Controller's Office](http://sfcontroller.org) maintains these codes in the [Executive Information System (EIS)](http://sfcontroller.org/divisions#accounting) where department staff maintain records related to spending, revenue and budget among other things. Other enterprise systems use these codes to link administrative data among departments.
 
## Reference

| Dataset | Description and Constraints | Reference Columns |
| :--- | :--- | :--- |
| [Department Code List](https://data.sfgov.org/City-Management-and-Ethics/Department-Code-List/j2hz-23ps) | <p>These department codes are maintained in the City's Financial System of Record. Department Groups, Divisions, Sections, Units, Sub Units and Departments are nested in the dataset from left to right. Each nested unit has both a code and an associated name.</p> <p>The dataset represents a flattened tree (hierarchy) so that each leaf on the tree has it's own row. Thus certain rows will have repeated codes across columns. Data changes as needed.</p> | Nested (right to left): `department_group_code` `division_code` `section_code` `unit_code` `sub_unit_code` `department_code` |
