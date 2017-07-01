# Documentation conventions

## About

There are many Unix-inspired documentation conventions around, every one slightly differing from others.

In this document, I have described conventions I follow in my ([RemekGdansk](github.com/RemekGdansk)) projects.

I have chosen a variant that does not rely on formatting (**bold**, _italic_) to convey all necessary information, so it can be used in plain text files.

Examples are provided with well-known Bash commands.

## Conventions - brief

No special characters: type exactly as written.

`<>` : substitute with custom value.

`[]` : optional to use.

`{}` : mandatory to choose one and only one option.

`|` : character to separate options.

`...` : use many times.

## Conventions - detailed

### Type exactly as written

Used to define words that are madnatory and need to be inserted without any alteration.

Syntax: `text`

Example: `ls`

### Substitute with custom value

Used to define placeholders and provide hints to insert mandatory custom values.

Syntax: `<text>`

Example: `touch <path>`

### Optional and to type exactly as written

Used for arguments that are optional, but if used, need to be written without any alteration.

Syntax: `[argument]`

Example: `ls [-l]`

### Optional and to substitute with custom value

Used for placeholders for optional arguments.

Syntax: `[<argument>]`

Example: `ls [<path>]`

### Zero to many alternative options

Pipe character `|` is used to separate list of optional arguments. Zero, one or more arguments can be used. Note that `<placeholder>` can be used in arguments list as well.

Syntax: `[option1|option2]`

Example: `ls [-a|-l|<path>]`

Equivalent: `[option1] [option2]`

### Mandatory, mutually excluding options

Used to mark that it is mandatory to choose one of the options.

Syntax: `{option1|option2}`

Example: `shutdown {<time>|now}`

### Optional, mutually excluding options

It is not mandatory to choose any option, but if chosen, only one can be used.

Syntax: `[{option1|option2}]`

### Repeated argument, use at least once

Used if argument can be repeated arbitrary number of times, but needs to appear at least once.

Syntax: `argument...`

Example: `touch <path>...`

### Repeated argument, does not have to appear at all

Used if argument can be repeated arbitrary number of times or it can be not used at all.

Syntax: `[argument]...`

Example: `ls [<path>]...`
