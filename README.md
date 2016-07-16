# DB_driver-fix-for-Grocery_CRUD

This is an alpha fix for the **Grocery_CRUD dbprefix known issue** with CodeIgniter Framework and a table prefix in the database configuration.

The problem is described here: 
<a href="https://github.com/scoumbourdis/grocery-crud/issues/66" target="_blank">https://github.com/scoumbourdis/grocery-crud/issues/66</a>

And here:
<a href="http://www.grocerycrud.com/forums/topic/436-problem-with-specific-table-name-bug-with-fix/" target="_blank">http://www.grocerycrud.com/forums/topic/436-problem-with-specific-table-name-bug-with-fix/</a>

It's an old topic, but the problem doesn't seem to be solved "officially" and i haven't found any useful solution
to keep using dbprefix without writing it in every single query in CI_Models, what makes very hard tu use thid part
modules or libraries which use database configurations.

This solution makes possible to use CI_Model's as usual, **without** specify the dbprefix, and Grocery_CRUD **with** the dbprefix.

I've modifies the function _protect_identifiers(...)_ in _system_folder_\database\DB_driver.php and it's marked on comments in the file. 
Search for the **//MOD** comments on code.

Feel free to modify/comment/criticize/test it.

**NOTE:**

Maybe it's not the best way to do this, and i've not tested in every possible way, but for basic operations, this works form me. I'll will update as i find new issues.
