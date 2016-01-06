# SafetyNet
Free yourself from runtime errors of the .NET ecosystem

SafetyNet is a .NET assembly of extensions and libraries (created in F#) for the .NET ecosystem that helps resolve many bugs related to null 
reference and conversion errors at runtime.

> **Advantages:**

> - Write cleaner and more maintainable code with less effort.
> - Nothing new to learn.
> - Works with all .NET languages.
> - Peform safe alternatives to common methods that would normally result in a runtime exception.
> - Helpful for F# when interop with C# assemblies.
> - Stop writing defensive code when you don't need to.
> - Provides OO and Functional style implementations.
> - Confidentially ship production code.

#Examples
**Cleaner and more maintainable code**

Typical examples

instead of:
```cs  
string[] myStrings = null;
var howMany = myStrings.Count();  // results in a runtime exception
```  
or -

```cs   
string[] myStrings = null;
var howMany = 0;
if(myStrings != null)
{
   howMany = myStrings.Count();  // defensive coding, lots of noise
}
```

using SafetyNet:
```cs  
string[] myStrings = null;
var howMany = myStrings.SafeCount();  // returns 0 in case of null (no runtime exception)
```

# What about C# 6+?
C# 6+ provides many great new features and ways to handle nulls like this:
```cs
List<string> myList = null;
var count = myList?.Count();  // Pure awesome, no runtime error
```

If you are able to utilize the newer framework, by all means use this new built-in syntax, 
however SafetyNet also provides complimentary and additional functionality for the latest .NET languages
such as:

> **Other Features:**
> 1
