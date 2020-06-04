# SimpleDependencyInjection
Just a very simple DI library i use across my projects.

## Usage

### Caching
```csharp
using SimpleDependencyInjection;

namespace SomeNamespace
{
    public class Class1
    {
        private SomeType someObject;

        public Class1()
        {
            DependencyContainer.Cache(someObject);

            var class2 = new Class2();
        }
    }
}
```

### Resolving
```csharp
using SimpleDependencyInjection;

namespace SomeNamespace
{
    public class Class2
    {
        private SomeType someObject;

        public Class2()
        {
            someObject = DependencyContainer.Get<SomeType>();
        }
    }
}
```
