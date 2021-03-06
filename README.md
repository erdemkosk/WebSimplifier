# WebSimplifier
A lightweight and easy-to-use web library for ASP .NET. It contains commonly used methods(like mail,time,password generator, etc..) for the website.


Instructions
============
When I developed my personal blog and resume web site, I realize that, always repeat myself for convert server time to local time or sending e-mail. In spite of getting bored, I decided to develop a library so that every developer can use it.

### SlugHelper

> It generate Url slug for routing process.

```sh
string generatedLink = UrlSlugManager.GenerateSlug("test slug string example");
```

### RandomKey

> It generate random keys or password. It supports all different possibility. (Upper- lower-numeric-special and all combination). There >are 15 different combination.

```sh
string generatedRandomKey = RandomKeyGeneratorManager.GenerateRandomKey(10,GenerationKeyType.LowerCasesAndSpecialWordsAndNumeric);
```

### LocalTime

> It can be used for getting local time for special time zones. *[Microsoft Time zone] for learning all time zones.

```sh
Console.WriteLine(TimeManager.GetLocalTime("Turkey Standard Time"));
Console.WriteLine(TimeManager.GetLocalTime("Eastern Standard Time"));
```

### JsonLogger

> Whenever an error is encountered, it records all the errors for logging.

```sh
JsonLogManager.LogPathFile =  @"C:\Users\mek\Desktop\errorLog.json";


 try
 {
      int numberForDivide = 20;
      int zero = 0;
      int sum = numberForDivide / zero;
  }
  catch (Exception ex)
  {
      JsonLogManager.LogError(ex);
      throw;       
  }
```

 [Microsoft Time zone]: <https://msdn.microsoft.com/en-us/library/ms912391(v=winembedded.11).aspx>
