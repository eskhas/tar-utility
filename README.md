# tar-utility

I created this linux utility tool as a project for system programming course in my university. 

### Usage:
```
sudo make install
tarsau –b t1 t2 t3 t4.txt t5.dat –o s1.sau
tarsau –a s1.sau d1
```
### Requirements:
- Ability to create an archive from specific files with a maximum file count of 32 and a total size
limit of 200 MB.
- Only text files which only have ASCII will be archived.
- Ability to extract files from an existing archive.
- Archive file must have enough information to recreate the archived files.

### Design:
  The tarsau was designed with this structure:
- Main Function (main): Handles command-line arguments and determines the operation type.
- Archive Creation (-b): Creates an archive file, checks file count and size limits, and writes
metadata and file contents to the archive.
- Archive Extraction (-a): Extracts files from an existing archive, validates directory existence,
and recreates the directory structure.
