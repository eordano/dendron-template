---
id: 683740e3-70ce-4a47-a1f4-1f140e80b558
title: Faq
desc: ''
updated: 1595952505025
created: 1595952505025
nav_order: 6
---
# FAQ

All the questions we thought you might ask. 

## General

### What is Dendron?

Dendron is a local-first, markdown based, hierarchical note taking tool. It is meant to help you organize, manage, publish, and collaborate on knowledge bases of any size.

### How is Dendron different from X note taking tool?

Substitute X with `roam|obsidian|foam|one note|evernote|...`

Dendron is focused on helping you **organize your notes** after they are **inside your knowledge base**.

Generally, the pattern for any note taking tool is that the **more notes you put it**, the **harder it becomes** to get anything **back out** again. 

Whether you are using notebooks or graphs, once you have more than a few hundred notes, you'll need to have some sort of structure in place (eg. naming convention, hierarchy, etc) to keep track of it. 

Dendron is designed to help you track your notes using hierarchies and enforce a consistent structure across your knowledge base. As an example, the author [@kevins8](https://twitter.com/kevins8) uses Dendron to manage +20K notes. 


### How does Dendron help me track my notes?

1. Dendron organizes and collapse all your  notes into managable chunks using [[hiearchies | dendron.topic.hierarchies ]].
2. Dendron helps you manage your hiearchies using [[schemas | dendron.topic.schema ]]
3. Dendron gets out of your way when your working with your notes during [[lookup |dendron.topic.lookup]]

You can read more about how all of this comes together in the [[ zen of dendron |dendron.zen]].

## Working with notes

### Why markdown?

Markdown lets you write text in a simple human readable notation that is platform independent. You don't need to have microsoft word to read a markdown file and now a days, all new note taking tools support importing and displaying markdown.

For more context, you can see the original markdown declaration here: https://daringfireball.net/projects/markdown/

### Can I use Dendron with existing notes?

You can use Dendron with existing repositories of markdown notes.

Open the `Command Bar` in vscode and use the `Dendron: Change Workspace` command. It will ask you for a folder path as input.

Dendron will create a `dendron.code-workspace` file in specified directory and then open the workspace (if a workspace file already exists, it will use that). It will also create a `root.md` file in that directory if it doesn't exist (currently this is part of the internal working of dendron).

Dendron **does not** delete or overwrite any files during the **Change Workspace** operation.

### How do I save?
- Dendron automatically saves when you change focus (switch tabs or applications). You can also manually save using `CMD+S` or `CTRL+S` depending on your operating system

## Misc

### Why does Dendron create `root.*` files in my vault?
- Dendron currently creates a `root.md` file and a `root.schema.yml` file where you initialize your vault. these files will be used in the future to automatically generate an index of everything in your vault. you may safely ignore them for now

### What is the extra text that is created at the beginning of each note?
- currently, you might see the following text added to the top of your note. This is additional metadata that Dendron uses to manage your files. 

```yml
---
id: 4407f75d-7334-47a5-9f19-18b458618136
title: dendron.lookup.hello
desc: ''
updated: 1594078624566
created: 1594078624566
data: {}
custom: {}
fname: dendron.lookup.hello
parent: null
children: []
---
```

### Why are there two `book` icons that do markdown preview?

We use an extension to do markdown preview. VSCode comes with its default markdown preview extension and its not currently possible to hide the button. You can re-open and upvote the issue [here](https://github.com/microsoft/vscode/issues/86994) if you want to fix this.

### How are hierarchies created?

Hierarchies today are created automatically when dendron crawls your folder for `.` delimited file names and custom schema.yml files.