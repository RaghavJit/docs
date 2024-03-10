# Naming Conventions

This file contains the rules for naming variables, files, tables, hooks, endpoints and functions etc. These conventions must be abided to strictly so the codebase remains easy to work with.

## Naming Variables

**Global variables**: All global variables must be named in capital letters in snake case. 
```
GLOBAL_VARIABLE
```

**Environment variables**: Names just like global variables but should start with 'ENV_'.
```
ENV_VARIABLE_NAME
```

**Local variables**: Should be named in pascal case.
```
LocalVariable
```

**Functions**: Should follow camel case.
```
sampleFunction()
```

**Event handling functions**: Should be named just like regular functions but name must begin with 'handle'.
```
handleClick()
```

**Hooks**: Hook name must be named in camel case and change hook function must begin with 'set'.
```
[userInformation, setUserInformation] = useState(null);
```

**Component Names**: All component must be names in pascal case.
```
ComponentName
```

**Pages**: Page names must follow lower snake case.
```
user_profile
```

**JSON Objects**: All json objects must be named like local variable or global variables depending on their use, but the attributes of a JSON object must be in snake case.
```
{
    name: "RaghavJit",
    age: 21
    home_address: "planet earth"
}
```
check out json objects conventions [here](./CodingConventions.md#JSON-objects)

