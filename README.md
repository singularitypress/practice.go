# Go

This repo is going to be a testing ground for learning the fundamentals of GoLang and the toolset. This "project" is being done in VSCode with tools/extensions by Google's Go team.

## Go CLI

A glossary of tools we'll have available to us.

- `go build` compiles the Go source code into a binary
- `go run` compiles and executes one or two files
- `go fmt` Formats the code in each file in the directory
- `go install` Compiles and "installs" a package, not unlike npm/nodejs
- `go get` downloads the source code of someone elses package
- `go test` runs any tests associated with the project

## Package

Think of `package <name>` as a way of declaring your project name- i.e. the `name` of your project in a `package.json` file. In Go, we're going to have to ensure that `package <name>` remains at the top of whatever Go source files we work with in said project.

### Why "package main"?

There's two types of packages, reusable and executable. The former is great for building reusable helper libraries, and the latter you'd want to use as your actual "main" project that you'd be able to make a binary.

### How about `func main()`?

Remember C++? Same thing, the "root" function's name is `main`.

## Variables

### Variable Declarations

Two ways:

1. `var card string = "Queen of Hearts"`
2. `card := "Queen of Hearts"`

### Arrays/Slices

In JS/TS we're typically accustomed to seeing `slice` as an `array` function with `arrays` themselves as being resizable. In Go, `Arrays` are fixed in size and type, while `Slices` are arrays that are dynamic in size but still fixed in type.

Note, the `append` function for slices doesn't modify the original `slice`, it returns a new one.

### for loops

```go
  for i, card := range cards {
		fmt.Println(i, card)
	}
```

- `i` is the index of the element in the array we're currently on
- `card` is the current item in the slice/array we're iterating over
- `range cards` says to take the slice of `cards` and loop over it
- code inside the `{}` is just code that runs over each iteration of the loop
