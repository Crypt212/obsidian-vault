- **Multer** is [[Node JS]] **[[middleware]]** for handling multipart/form-data, which is primarily used for uploading files.
# Usage
- Multer adds a `body` object and a `file` or `files` object to the `request` object. The `body` object contains the values of the text fields of the form, the `file` or `files` object contains the files uploaded via the form.
# Important Notes
- The from sent must have `multipart/form-data` encryption type.
- 