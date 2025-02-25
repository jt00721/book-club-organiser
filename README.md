# book-club-organiser
The Book Club Organiser will allow users to add books, schedule reading discussions, track reading progress, and mark books as completed. This project will use only Golang's standard libraries (no external web frameworks like gin, no ORMs like gorm) to build a fully functional CRUD web app with structured content management.

## Core Goals:

- Allow users to add, edit, and delete books from a reading list.
- Schedule discussion dates for each book.
- Track reading progress and mark books as completed.
- Store book details in an SQLite database using database/sql.
- Build a simple, clean UI using Golang's html/template and standard libraries.

## Project Breakdown by Day
### Define Scope & Set Up Project

✅ Goals:

    Plan out the Book Club Organizer’s features.
    Initialize the project without external dependencies.
    Set up a basic project structure using standard Go libraries.

✅ Tasks:

    Define database schema (Books, Discussions, Reading Progress).
    Set up main.go and configure routing using net/http.
    Prepare basic HTML templates with html/template.

📌 Deliverable: Project is initialized with a clear scope & structure.

### Set Up Database & Models

✅ Goals:

    Use SQLite with database/sql to store book and discussion details.

✅ Tasks:

    Create database tables for:
        Books (ID, Title, Author, Status, Discussion Date)
        ReadingProgress (BookID, PagesRead, TotalPages)
        Discussions (BookID, DiscussionDate, Notes)
    Write raw SQL queries to create and manage these tables.
    Implement a database connection function using database/sql.

📌 Deliverable: A structured database schema set up using standard SQL queries.

### Implement Backend Logic (CRUD Operations)

✅ Goals:

    Implement CRUD operations for books and discussions using net/http and database/sql.

✅ Tasks:

    Create HTTP handlers for:
        POST /books → Add a new book
        GET /books → Fetch all books
        PUT /books/:id → Edit book details (title, author, status)
        DELETE /books/:id → Remove a book
        POST /discussions → Add a discussion for a book
        GET /discussions/:bookID → Retrieve discussions for a book
    Use Go’s http.ServeMux for routing (no external router).
    Handle form submissions using r.FormValue() for adding books and discussions.

📌 Deliverable: A fully functional backend using only standard libraries.

### Build the UI & Connect to Backend

✅ Goals:

    Use html/template to dynamically display books and discussions.

✅ Tasks:

    Create HTML templates for:
        Homepage (list of books + reading status)
        Add new book page
        Discussion page (list discussions per book)
        Progress tracking page
    Use Go’s template syntax ({{.}}) to dynamically load book data.
    Implement basic CSS styling for better UI experience.

📌 Deliverable: A working frontend integrated with backend data.

### Implement Reading Progress & Book Completion Tracking

✅ Goals:

    Allow users to track how much they’ve read.
    Users can mark books as completed.

✅ Tasks:

    Add a progress tracking feature (UPDATE progress in ReadingProgress table).
    Implement a checkbox/button to mark books as "Completed".
    Display progress bars (e.g., "You’ve read 150/300 pages").
    Store progress updates using database/sql.

📌 Deliverable: A fully functional progress tracker inside the Book Club Organizer.

### Testing, Debugging & UI Enhancements

✅ Goals:

    Fix bugs and UI issues, test edge cases.

✅ Tasks:

    Test all CRUD operations manually.
    Debug database queries & ensure data is stored correctly.
    Improve form validation (e.g., prevent empty book titles).
    Enhance UI with CSS refinements.

📌 Deliverable: A clean, polished, and fully tested Book Club Organizer.

### Final Testing & Project Wrap-Up

✅ Goals:

    Perform final optimizations.

✅ Tasks:

    Test multiple users adding books & discussions.
    Ensure SQL queries are optimized for performance.
    Record a recap video showcasing how the Book Club Organizer works.

📌 Deliverable: Final working Book Club Organizer ready for deployment.
