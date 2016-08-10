# xmldoc-snippets
Atom XML-Doc snippets intended for C#.

## References
XML Doc documentation:   https://msdn.microsoft.com/de-de/library/b2s063f7(v=vs.71).aspx  
XML Doc examples:        https://msdn.microsoft.com/en-us/library/b2s063f7(v=VS.100).aspx

## Remarks
This does not support lists and includes.

## Usage
``` csharp
snippet
-----------------------------------------
result
```

### Modular snippets

``` csharp
///s
-----------------------------------------
/// <summary>
/// ${1:General description}
/// </summary>$2
```

``` csharp
///re
-----------------------------------------
/// <remarks>
/// ${1:Detailed remarks}
/// </remarks>$2
```

``` csharp
///r
-----------------------------------------
/// <returns>
/// ${1:Return value description}
/// </returns>$2
```

``` csharp
///pa
-----------------------------------------
/// <param name="${1:Param name}">${2:Param description}</param>$3
```

``` csharp
///ex
-----------------------------------------
/// <exception cref="${1:Exception type}">Thrown when ${2:condition}</exception>$3```

``` csharp
///sea
-----------------------------------------
/// <seealso cref="${1:Ref name}">
/// ${2:Ref description}
/// </seealso>$3
```

``` csharp
///e
-----------------------------------------
/// <example>
/// ${1:Example description}
/// <code>
/// ${2:Code}
/// </code>
/// </example>$3
```

### Inline snippets
``` csharp
see
-----------------------------------------
<see cref="${1:Ref name}"/>$2
```

``` csharp
paramref
-----------------------------------------
<paramref name="${1:Ref name}"/>$2
```

``` csharp
para
-----------------------------------------
<para>${1:Content}</para>$2
```

``` csharp
permission
-----------------------------------------
<permission cref="${1:Permission type}">${2:Description}</permission>$3
```

### Semantic snippets
``` csharp
///a            // For use on an action
-----------------------------------------
/// <summary>
/// ${1:Action description}
/// </summary>
/// <param name="${2:Param name}">${3:Param description}</param>$4
```

``` csharp
///f            // For use on a function
-----------------------------------------
/// <summary>
/// ${1:Function description}
/// </summary>
/// <param name="${2:Param name}">${3:Param description}</param>
/// <returns>
/// ${4:Return value description}
/// </returns>$5
```

``` csharp
///p             // For use on properties
-----------------------------------------
/// <summary>
/// ${1:Property description}
/// </summary>
/// <value>
/// ${2:Property value}
/// </value>$3
```
