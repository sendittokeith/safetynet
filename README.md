# SafetyNet
Free yourself from null hell of the .NET ecosystem

SafetyNet is a .NET assembly of extensions (created in F#) for the .NET ecosystem that helps resolve MANY bugs related to null reference errors at runtime in .NET.

> **Advantages:**

> - Cleaner and more maintainable code.  (mention defensive)
> - Nothing new to learn.
> - Works with all .NET languages.
> - Peform safe alternatives to common methods that would normally result in a runtime exception.
> - Confidentially ship production code

**Why?:** 

In my 14+ years of working with .NET (since beta) creating business lines of applications, I have rarely had the need to utilize nulls (less than .01% of the time).

#Examples?
**Cleaner and more maintainable code**

Stop writing defensive code when you don't need to.

Typical examples

instead of:
string[] myStrings = null;
var howMany = myStrings.Count();  // results in a runtime exception

defensive coding:

```cs   
string[] myStrings = null;
var howMany = 0;
if(myStrings != null)
{
   howMany = myStrings.Count();  // results in a runtime exception
}
```


using SafetyNet:
string[] myStrings = null;
var howMany = myStrings.SafeCount();  // returns 0 in case of null (no runtime exception)


