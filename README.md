This is a React functional component that displays a list of users and enables searching for users by city and sorting by name. It also allows displaying a specific number of users per page and navigating between pages.

First, React, useState and useEffect hooks are imported from React, as well as the axios library for making HTTP requests. A CSS file is also imported.

Then, the user type is defined using an interface which has an ID, name, address, phone, and company name.

After that, the App function component is defined which uses several useState hooks to store state.

The first useState hook stores the list of users, the second hook stores the search term for searching users.

The third hook stores the current page that the user is viewing, and the fourth hook stores the sorting direction. (ASC DESC)

Then, the useEffect hook is used, which is called only once during the initial rendering of the component.

This hook is used to retrieve the list of users using an HTTP GET request to the web API path 'https://jsonplaceholder.typicode.com/users'.

The results are stored in the user state. After that, several helper functions are defined.

handleSearchTermChange handles changes in the user search and sets the current page to the first page.

handleSortDirectionChange reverses the sorting direction.

sortedUsers and filteredUsers sort and filter users alphabetically and by city search using Array.sort() and Array.filter().

Finally, handlePageChange updates the current page when the user clicks the navigation button.

At the end of the App function, JSX is rendered which displays a search field, a table with the list of users, a navigation button and uses the stored values from the useState hooks and helper functions for dynamic data display.

Sorted users are displayed in the table with name, address, phone, and company name.

Also, an up or down arrow is displayed depending on the current sorting direction.

The navigation button is generated using the Array.from() and map() methods and adds the "active" CSS class to the current page.

This is a simple example of a functional React component that uses useState and useEffect hooks, an HTTP GET request, field sorting and filtering, and page navigation to display a list of users in a table.

To try this code out on your local machine, simply download the project, open it in your Visual Studio Code, and start it by tiping in your terminal
"npm start".

The main code is located in the file "App.tsx" in "src" folder. Style is located in the file "App.css" in the folder "src".
