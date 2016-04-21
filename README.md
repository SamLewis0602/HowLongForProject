# HowLongForProject
This project was entirely coded from scratch.
This is an application that students can use to add assignments with metadeta such as total completion time, difficult, and the grade they received. All assignments are then compiled and organized by professor, teacher, semester, and difficulty. The stats page shows general stats from all submissions, such as top 10 longest assignments, top 10 longest classes, top 10 most difficult classes, etc.

## Front-end
The front end uses jQuery for all DOM manipulation. Each tab at the top of our site (Browse, Search, Stats, Submit) is built to operate on a single page by only replacing the parts of the DOM that need to be updated.

## Back-end
The back end of this application uses a MySQL database. There is a table for each aspect of the database including assignment, professor, section, and more.

## API
The API in this application consists of several PHP files. HLFP.php is the main API file to which the front end makes AJAX calls. The rest of the files include several ORM layers to represent different tables in the database and abstract the logic to retrieve those items. All AJAX calls to the API will return a JSON object.

The API uses extra path info to determine what objects to return. It operates on the following format:
"HLFP.php/<return type>/<filter type>/<filter value>"
For example, "HLFP.php/class/department/5" will return all the classes in the department with an id of 5. More examples can be seen in the comments in HLFP.php.
