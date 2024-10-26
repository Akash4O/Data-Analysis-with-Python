## Importing Data:

    -> Process of loading and reading data into Python from various resources.

# Two important properties:

    -> Format
        
        -> various formats: .csv , .jason, .xlasv , .hdf ....

    -> File path of Dataset : it can be a local datasets path or a internet drive path or location of the dataset
        
        -> Computer: /Desktop/mydata.csv

        -> Internet: https://archive.ics.uci.edu/autos/imports-85.data

## Importing And Exporting a csv into Python :

    -> For the purpose of importing csv file we are using pandas library in python.

    -> In pandas we have a function "read_csv()" function to read the files

**Sample python program for importing Data Set Udsing pandas:**

    import pandas as pd
    
    path = "https://github.com/Akash4O/Data-Analysis-with-Python/blob/main/module%201/imports_85_data.csv"

    fd = pd.read_csv(path, header=None) // the read_csv assumes that the data contains a header 

    //but in our data there are no headers so we have specified "header=None"

**Printing the dataframe in Python :**

    // df prints the entire dataframe(not recommended for large datasets)
    
    // instead we can use df.head(n) function to show the first n data frame

    // Wiseverse with df.tail(n) which shows the bottom n data frames

    df.head(5)

    df.tail(5)

**Adding headers :**

    // Replace default header (by df.columns = headers)

    headers=["symboling","normalized-losses", "make", "fuel-type", "aspiration", "num-of-doors", "body-style", "drive-wheels", "engine-location", "wheel-base", "length", "width", "height", "curb-weight", "engine-type", "num-of-cylinders", "engine-size", "fuel-system", "bore", "stroke", "compression-ratio", "horsepower", "peak- rpm","city-mpg", "highway-mpg","price"]

    df.columns = headers

    df.head(5) // printing the values to see whether the headers appended or not

**Exporting a Pandas Dataframe to CSV :**

    //Preserve progress anytime by saving modified dataset using

    path = "C:\windows\....\automobile.csv"

    df.to_csv(path) // using to_csv() we can save the performed data frame into csv file
