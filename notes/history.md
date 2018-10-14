```
[ 10:01am ]  [ kvogel@kvogel-macbook-2018:~/Projects/react-material(master✗) ]
 $ man history
[ 10:02am ]  [ kvogel@kvogel-macbook-2018:~/Projects/react-material(master✗) ]
 $ history --help
omz_history:fc:13: bad option: -h
[ 10:02am ]  [ kvogel@kvogel-macbook-2018:~/Projects/react-material(master✗) ]
 $ which history
history: aliased to omz_history
[ 10:02am ]  [ kvogel@kvogel-macbook-2018:~/Projects/react-material(master✗) ]
 $ which omz_history
omz_history () {
	local clear list
	zparseopts -E c=clear l=list
	if [[ -n "$clear" ]]
	then
		echo -n >| "$HISTFILE"
		echo History file deleted. Reload the session to see its effects. >&2
	elif [[ -n "$list" ]]
	then
		builtin fc "$@"
	else
		[[ ${@[-1]} = *[0-9]* ]] && builtin fc -l "$@" || builtin fc -l "$@" 1
	fi
}
[ 10:02am ]  [ kvogel@kvogel-macbook-2018:~/Projects/react-material(master✗) ]
 $ show omz_history
omz_history is at:
Usage: file [-bcEhikLlNnprsvzZ0] [-e test] [-f namefile] [-F separator] [-m magicfiles] [-M magicfiles] file...
       file -C -m magicfiles
Try `file --help' for more information.
mime type:
```

???