# 🐚 Minishell

la mini con el eneko: rebuilding our own **mini version of Bash** 💻

It must:
- Display a prompt and wait for user input 💬  
- Parse commands and arguments properly 🧩  
- Handle pipes `|` and redirections `<`, `>` `>>`, `<<`  
- Execute builtins and external programs ⚙️  
- Manage environment variables 🌱  
- Handle signals gracefully (Ctrl+C, Ctrl+D, Ctrl+\) ⚡  
- Never crash or leak memory 🧹  

---

## 💬 Example Session

```bash
$ ./minishell
minishell> echo Hello World
Hello World
minishell> export NAME=Nere
minishell> echo $NAME
Nere
minishell> ls | grep src
src
minishell> cat < infile | grep something > outfile
minishell> exit
```

## ⚙️ Implemented Builtins
  Your minishell must handle these built-in commands:
  Command	Description
      echo	Prints text to standard output
      cd	Changes the current directory
      pwd	Prints the current working directory
      export	Sets an environment variable
      unset	Removes an environment variable
      env	Displays environment variables
      exit	Exits the shell

## ⚒️ Allowed Functions
read, write, open, close, pipe, dup, dup2,
fork, execve, wait, waitpid, access,
signal, kill, exit, getenv, malloc, free, perror, strerror
Libft and gnl 

## ⚠️ Error Handling
    ❌ Invalid commands → "command not found"
    🚫 Wrong syntax → "syntax error near unexpected token"
    📂 File not found → "No such file or directory"
    🧹 No leaks allowed (check with valgrind)
    🧠 Handle Ctrl+C, Ctrl+D, and Ctrl+\ like Bash
