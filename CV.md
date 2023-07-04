# My Curriculum Vitae
 Curriculum Vitae

> # Maksakau Maksim
![Face Reveal]()
> ## Age: ???

__
> ### Contacts
* [Telegram](https://t.me/MMA2K2)
* [VK](https://vk.com/bluedrygloss)
* [GitHub](https://github.com/SOLDIEROFWW4)

__
> ## Something About Myself:
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

__
> ### My Skills:
1. [C# CodeWars 6kyu](https://www.codewars.com/users/GreyEyedAngel)
2. T-SQL (Microsoft SQL Server, Microsoft Access)

__
> ### Language Skills:
1. English Level: A2 (According to EPAM English  Test), B1 (According to A1QA English Speaking and Grammar Test)
2. Russian Level: C2 (Native Speaker)
3. Belarussian Level: C2 (Native Speaker)

> ### Solved CodeWars Katas (Code Example)
* How can you tell an extrovert from an introvert at NSA?
Va gur ryringbef, gur rkgebireg ybbxf ng gur BGURE thl'f fubrf.

* I found this joke on USENET, but the punchline is scrambled. Maybe you can decipher it?
According to Wikipedia, ROT13 is frequently used to obfuscate jokes on USENET.

* For this task you're only supposed to substitute characters. Not spaces, punctuation, numbers, etc.

```C#
public static string Rot13(string input)
  {
     char[] array = input.ToCharArray();
            for (int i = 0; i < array.Length; i++)
            {
                int number = (int)array[i];
                
                if (number >= 'a' && number <= 'z')
                {
                    if (number > 'm')
                    {
                        number -= 13;
                    }
                    else
                    {
                        number += 13;
                    }
                }
                else if (number >= 'A' && number <= 'Z')
                {
                    if (number > 'M')
                    {
                        number -= 13;
                    }
                    else
                    {
                        number += 13;
                    }
                }
                array[i] = (char)number;
            }
            return new string(array);
  }
```

* Complete the function scramble(str1, str2) that returns true if a portion of str1 characters can be rearranged to match str2, otherwise returns false.

```C#
public static bool Scramble(string str1, string str2) 
    {
        Dictionary<char, int> charCount = new Dictionary<char, int>();

            foreach (char c in str1)
            {
                if (charCount.ContainsKey(c))
                {
                    charCount[c]++;
                }

                else
                {
                    charCount[c] = 1;
                }
            }    

            foreach (char c in str2)
            {
                if (!charCount.ContainsKey(c) || charCount[c] == 0)
                {
                    return false;
                }
                charCount[c]--;   
            }

            return true;
    }
```

* The rgb function is incomplete. Complete it so that passing in RGB decimal values will result in a hexadecimal representation being returned. Valid decimal values for RGB are 0 - 255. Any values that fall out of that range must be rounded to the closest valid value.

* Note: Your answer should always be 6 characters long, the shorthand with 3 will not work here.

```C#
  public static string Rgb(int r, int g, int b) 
  {
    
    r = Math.Max(0, Math.Min(255, r));
    g = Math.Max(0, Math.Min(255, g));
    b = Math.Max(0, Math.Min(255, b));


    string hexValue = r.ToString("X2") + g.ToString("X2") + b.ToString("X2");

    return hexValue;
  }
```


