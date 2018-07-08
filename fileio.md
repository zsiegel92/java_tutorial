[All Lessons](https://zsiegel92.github.io/java_tutorial)

# File IO

[TOC]

## Getting user Input from Console

Some math $\frac{5}{2}$.

```python
def hello():
	return 5
```

and

```java
import java.io.File;
import java.io.IOException;
import java.util.Scanner;
import java.util.function.ToDoubleFunction;
import java.io.FileNotFoundException;

class Main {
    public static void main(String[] args) {
        System.out.println("Please enter some text");
        String text;
        Scanner inp = new Scanner(System.in);
        text = inp.nextLine();
        inp.close();
        System.out.println("You entered " + text);
    }
}
```

## Reading from a file using `Scanner`, counting number of lines, saving each line in an array

```java
import java.io.File;
import java.io.IOException;
import java.util.Scanner;
import java.io.FileNotFoundException;

class Main {
    public static void main(String[] args) throws FileNotFoundException {
        String fname = "data.txt";
        File file new File(fname);;
        Scanner sc = new Scanner(file);

        int counter = 0;
        while (sc.hasNextLine()) {
            counter++;
            sc.nextLine();
            sc.nextLine();
        }
        System.out.println("There are " + counter + " entries");

        sc = new Scanner(file);

        String[] lines = new String[counter];

        for (int i = 0; i < counter; i++) {
            try {
                lines[i] = sc.nextLine();
            } catch (Exception e) {
                System.out.println("Invalid input");
            }
        }
        sc.close();
    }
}
```

## Writing to a File using `PrintWriter`

```java
import java.io.PrintWriter;
import java.io.FileNotFoundException;
import java.io.UnsupportedEncodingException;

class Writer{


	public static void main(String[] args) throws FileNotFoundException,UnsupportedEncodingException{
		PrintWriter writer = new PrintWriter("the-file-name.txt", "UTF-8");
		writer.println("The first line");
		writer.println("The second line");
		writer.printf("hey %.2f",105.3);
		writer.close();
	}
}
```
