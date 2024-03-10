# Coding Conventions


## Spacing

**Operators**: All operators must have space around them like in the example below.
```
variable1 == variable2

condition1 && condition2

() => {}
```

**Code blocks**: A code block nested inside {}, <>, or tags must have a line above an below containing nothing but the continer symbol.
```
if (VariableName1 == VariableName2)
{                               // this line contains only '{'
    statement1;
    statement1;
    statement1;
    statement1;
}                               // this line contains only '}'
```

**Declaring Variables: Similar to all above '=' operators must have space around it. Also all the local and global variables must be written together in a block with an empty like above and below.
```
...

const VariableName1 = 'test';
const VariableName2 = 'blabla';
const VariableName3 = 'huehue';

...
```

**Managing blocks together**: If one code block is to be written after another they must be saprated by two (2) empty lines.
```
<div className="SidebarContainer">
    <MainSidebar filterByTag={filterByTag}/> 
</div>


<div>
    <MainNavbar/>
</div>
```

**Commas and Colons**: All commas must be followed by a space and should not have any spaces ahead, same implies for colons.
```
[item1, item2, item3]

name: "RaghavJit",
```

**Imports**: 
1. All first import statement must be in the first line of the file there must be no emply lines above the first import line. 
1. Similar imports must be grouped together and sparated from other types with a single empty line.
```
import {useState, useEffect} from 'react'; //importing inbuilt features

import MainNavbar from '../Components/Navbar.js'; //importing all components
import MainSidebar from "../Components/Sidebar.js";
import ProjectTemplate from "../Components/ProjectTemplate.js";

import "../styles/GlobalStyles.css" //importing style sheets
```


## Identation

1. One tab corrusponds to 4 spaces, don't use spaces when providing identation use Tab instead.
2. Every child block must be one (1) identation level deeper then the parent.
3. If a block is not contained in a parent it must not have any identation.


## JSON-objects

1. JSON objects must be named like regular variables and should follow either local variable convention or global variable convention depending on their use. 
1. However the attributes of the JSON object must always be in 'snake_case'
1. Every nested attribute must be a one (1) identation level deeper than the parent. (see address attribute)
1. Lists in JSON objects must be one line (see hobbies attribute)
1. It must follow the spacing scheme for commas and colons as specified above.
1. String attribute must be enclosed in "", **using '' or `` is NOT allowed**.
1. Numbers must not be enclosed in "" (see age and zipcode)
```
{
    "name": "John Doe",
    "age": 30,
    "city": "New York",
    "is_student": false,
    "hobbies": ["reading", "traveling", "coding"],
    "address": {
        "street": "123 Main Street",
        "city": "Anytown",
        "zipcode": 12345
    }
}
```


## Components

1. All components must be imported together (as specified in Spacing/Imports above)
1. While passing props to the component, one prop must take one line, one identation deeper that component.
1. There must be empty line above and below, if the component is not eclosed in a map or filter function.
```

<GatsbyImage 
    image={getImage(props.fi_path)} 
    alt="featured image"
/> 

```


## Map and Filter

1. Always specify the format of the object or array that is being mapped in a comment above the map fucntion.
1. Leave one line above and below this block
```
...

// TagsList = ["tag1", "tag2", "tag3"]
{
    TagsList.map((tag, index) => 
        <PostLabel 
            key={index} 
            title={tag} 
            filterPosts={props.filterResponse}
        />)
}

...
```
1. If using multiple function they must be in single line.
```
{
    CurrentPosts.slice(ShowPages.from, ShowPages.to).map(({node}) =>  //slice and map in single line
        <PostTemplate 
            key={node.frontmatter.slug} 
            slug={node.frontmatter.slug} 
            fi_path={node.frontmatter.fi_path} 
            title={node.frontmatter.title} 
            tags={node.frontmatter.tags} 
            filterResponse={filterByTag} 
            info={node.frontmatter.info}
            date={node.frontmatter.date} 
            snippet={node.excerpt}
        />)
}  
```


## Delaring Hooks and Functions

1. All the useState hooks must be written together with empty line above and below the group just like local variables are written.
```
...

const [vantaEffect, setVantaEffect] = useState(null) 
const [vantaEffect, setVantaEffect] = useState(null) 
const [vantaEffect, setVantaEffect] = useState(null) 

...
```
2. All useEffect hooks must have one empty line above and below them
```

useEffect(() => {
    
    statement1
    statement2
    statement3
    statement4

}, [data, featuredData, labelData]) // useEffect array must be in last line
```
