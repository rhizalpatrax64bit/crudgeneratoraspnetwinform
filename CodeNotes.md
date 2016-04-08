#Unique File Name Getter

# Introduction #

This bit of C# code returns a new file path in case you need to not overwrite existing file names.  For example, if you pass in "c:\test.txt" - a file which exists, this function returns "c:\test\_2.txt".

```
        /// <summary>Checks if the file exists, and if it does, appends a number to the end of the file name
        /// </summary>
        /// <param name="fileName">Fully qualified file path</param>
        /// <returns></returns>
        public string GetNonConflictingFileName(string fileName) {
            FileInfo finfo = new FileInfo(fileName);
            string justFileName = finfo.Name.Replace(finfo.Extension, "");
            int i=2;
            while (finfo.Exists){
                fileName = string.Format("{0}\\{1}_{2}{3}",
                    finfo.Directory, justFileName, i, finfo.Extension);
                finfo = new FileInfo(fileName);
                i++;
            }
            return fileName;

        }
```