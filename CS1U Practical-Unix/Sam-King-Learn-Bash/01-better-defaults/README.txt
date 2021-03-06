Read each of the files in this directory. Try executing them, and see if the result is what you expect.


Bash was desugned as a shell rather than as a programming language, so it tends to be permissive with errors (e.g., a user who mistypes a shell command should not have their whole shell crash). That does not always make sense for scripts.


After reading through each of the scripts in this directory, try adding the following line to the top and then re-running them.

set -euxo pipefail

That will set the defaults so that scripts fail faster.

	-e sets it to fail on errors
	-u sets it to fail on unset variables
	-x sets it to print out every command that is executed. This is great in some cases, but there are also definitely times when you don't want to set -x.
	-o pipefail sets it to fail when any command in a pipeline fails


For more on this subject, check out
http://redsymbol.net/articles/unofficial-bash-strict-mode/
