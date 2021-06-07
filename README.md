# first-assignment- 


The program : 


    #include <stdio.h>
    #include <stdlib.h>

    int main()
      {
          FILE * file;
          char path[100];

          char ch;
          int characters, words, lines;


          /* Input path of files to merge to third file */
          printf("Enter source file path: ");
          scanf("%s", path);

          /* Open source files in 'r' mode */
          file = fopen(path, "r");


          /* Check if file opened successfully */
          if (file == NULL)
          {
              printf("\nUnable to open file.\n");
              printf("Please check if file exists and you have read privilege.\n");

              exit(EXIT_FAILURE);
          }
          characters = words = lines = 0;
          while ((ch = fgetc(file)) != EOF)
          {
              characters++;
              if (ch == '\n' || ch == '\0')
                  lines++;

              /* Check words */
              if (ch == ' ' || ch == '\t' || ch == '\n' || ch == '\0')
                  words++;
          }

         
          if (characters > 0)
          {
              words++;
              lines++;
          }

          /* Print file */
          printf("\n");
          printf("Total characters = %d\n", characters);
          printf("Total words      = %d\n", words);
          printf("Total lines      = %d\n", lines);


          /* Close files to release resources */
          fclose(file);

          return 0;
      } 
      
      
      
      
   ![1](https://user-images.githubusercontent.com/85512440/121068586-f1b36180-c778-11eb-9a03-9d2436e22bb4.png)
      
      
      
      
   ![2](https://user-images.githubusercontent.com/85512440/121068615-f7a94280-c778-11eb-806d-b6ba49431e65.png)
      
      
      
      
      
      
   ![3](https://user-images.githubusercontent.com/85512440/121068627-fd068d00-c778-11eb-966d-c37f649d6ba7.png)


