# Domain Storytelling with PlantUML

DomainStory-PlantUML uses [PlantUML](http://en.plantuml.com/) to describe and
document a domain story which was developed in a
[Domain Storytelling](http://www.domainstorytelling.org) workshop.

DomainStory-PlantUML includes macros for creating domain stories with PlantUML.

* [Getting Started](#getting-started)
* [License](#license)

## Getting Started

At the top of your domain story PlantUML `.puml` file,
you need to include the `domainStory.puml` file
found in the `root` of this repo.

To be independent of any internet connectivity,
you can also download the files found in the `root`
and reference it locally with

```c#
!include path/to/domainStory.puml
```

Just remember to change the `!include` statements inside the top of the files.

If you want to use the always up-to-date version in this repo, use the following:

```c#
!includeurl https://raw.githubusercontent.com/johthor/DomainStory-PlantUML/master/domainStory.puml
```

Now let's create a domain story diagram:

After you have included `domainStory.puml` you can use the defined macro
definitions for the domain story actors: `Person`, `Group`, and `System`.
As well as the work items: 
`Document`, `Folder`, `Call`, `Email`, `Conversation`, and `Info`

```csharp
@startuml Pictografic_Language
!includeurl https://raw.githubusercontent.com/johthor/DomainStory-PlantUML/master/domainStory.puml

node actors
Person("PersonLabel")
Group("GroupLabel")
System("SystemLabel")

node "work objects"
Document("DocumentLabel") 
Folder("FolderLabel") 
Call("CallLabel") 
Email("EmailLabel") 
Conversation("ConversationLabel") 
Info("InfoLabel") 

node others
Person(personAlias, "Label", "Optional Description")
@enduml
```

## License

This project is licensed under the MIT License
- see the [LICENSE](LICENSE) file for details
