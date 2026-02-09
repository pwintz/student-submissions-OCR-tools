Repository for OCR script that splits student submissions from one PDF into a PDF for each student.

# Setup
1. Clone this repository.
2. Add the list of student names to `student_names.user-words` (One line per name. First and last names on separate lines). 
3. Tell Git not to ignore changes to `student_names.user-words` by running `git update-index --skip-worktree student_names.user-words`.

Install `Tesseract` and `pdftk`.

# Usage

## PDF Creation
Create PDFs with student names at fixed locations.

## PDF Separation
Add a PDF to `in_dir`.

# Setup for start of a new class

1. Add all of the students names to `student_names.user-words`

# Troubleshooting:

**Problem:** A page is placed into the wrong student 
**Solution:** 

1. Run the initial pass of OCR with `regenerate_page_lists=true`. 
2. Set `regenerate_page_lists=false` and modify the `.txt` files in `student_page_lists`. 
3. Run OCR again.