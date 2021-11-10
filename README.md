The program was written in python 3.9 using Sublime text editor on Mac. 
 You can run this code in Sublime text by using 'Build' under tools or using Ctrl +B

```
import csv
from itertools import zip_longest         

c1 =[]
c2 = []
c3=[]
d= [c1, c2,c3]


with open ('movies_metadata_sample.csv','r') as f: #to open and read given csv file
	reader = csv.reader(f,delimiter = ',')
	next(reader)
	for row in reader:
		c1.append(row[3]) 
		c2.append(row[14]) 
		c3.append(row[23])
		zip(*c1)
export_data= zip_longest(*d,fillvalue= '')

with open('new_movie_list.csv','w',newline = '')as f:        #creates new csv file 
  
   write = csv.writer(f,delimiter=",")           
        
   write.writerow(("Genres","Year","Count"))      #creates header

   write.writerows(export_data)                       #exports selected data into new csv file
   ```
   The resulting output can be viewed below
   
   [new_movie_list.csv](https://github.com/rachelibarbia/movies1/files/7509631/new_movie_list.csv)

