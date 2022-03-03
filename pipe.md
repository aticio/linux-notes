| pipe symbol

gets the output from the given command and passes that as an input

*command-output | command-input*

stderr won't given to the pipe by default. You need to append stdin and stderr and then apply pipe to the output. [[IO]]

----------------------------

[[grep]]
*grep pattern file* is same with
*cat file | grep pattern*