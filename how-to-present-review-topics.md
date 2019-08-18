# How to present a topic on review day

## Overview

- Practice explaining things as you would to a job interviewer
- At a minimum, go into as much detail as we covered in class
- Ideally do some additional research and teach us something new :)

## First define the concept

Let's use `cp` as an example.

### Background

- Tell us something about the context in which it's relevant?

  E.g. It's a UNIX command for working with the file system

- Is it related to other familiar concepts?

  E.g. It has some similarities to `mv`, `touch` and `mkdir` (they are also UNIX commands that alter the file system)

### Purpose

- What is its primary purpose (when should we use it)?

  E.g. It allows you to copy files

- What are some things to be careful of (when should we not use it)?

  E.g. This command can overwrite existing files without warning.
  To avoid this, make sure that you specify a destination that does not exist yet (or one that you definitely intend to replace)

## Then demonstrate usage

Live code examples of different use cases. For command line tools, consider different kinds of arguments and different flags.

E.g.

- `cp source_file target_file`
- `cp source_path target_path`
- `cp -R source_dir existing_target_dir`
- `cp source_file target_dir`
- `cp source_file_one source_file_two target_dir`

Also show some common gotchas (pitfalls) and how to resolve them.

E.g.
  
- `cp source_file existing_file` (this overwrites the existing file)
- `cp source_dir new_target_dir` (won't work, must run `mkdir`)
- `cp -R source_dir target_dir` (without `/` the whole dir is copied)
- `cp -R source_dir/ target_dir` (with `/` only the contents of the dir are copied)
