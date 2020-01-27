`# Show current Git branch at command prompt
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/\1/'
}
export PS1="\[\033[01;32m\]\u: \[\033[01;36m\]\w \[\033[01;33m\]branch:(\[\033[00;33m\]\$(parse_git_branch)\[\033[01;33m\])\[\033[00m\] \n$ "`