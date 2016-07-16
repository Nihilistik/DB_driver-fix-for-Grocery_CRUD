# DB_driver-fix-for-Grocery_CRUD

This is an alpha fix for the **Grocery_CRUD dbprefix known issue** with CodeIgniter Framework and a table prefix in the database configuration.

The problem is described here: 
<a href="https://github.com/scoumbourdis/grocery-crud/issues/66" target="_blank">https://github.com/scoumbourdis/grocery-crud/issues/66</a>

And here:
<a href="http://www.grocerycrud.com/forums/topic/436-problem-with-specific-table-name-bug-with-fix/" target="_blank">http://www.grocerycrud.com/forums/topic/436-problem-with-specific-table-name-bug-with-fix/</a>

It's an old topic, but the problem doesn't seem to be solved "officially" and i haven't found any useful solution
to keep using dbprefix without writing it in every single query in CI_Models, what makes very hard tu use thid part
modules or libraries which use database configurations.

I've modifies the function _protect_identifiers(...)_ and it's marked on comments in the file. 
Search for the **//MOD** comments on code.

Feel free to modify/comment/criticize/test it.

**NOTE:**
It's tested only in basic CRUD operations, and i'll update things as i'll go in advanced operations like 
relations.
