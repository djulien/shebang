# shebang
Shebang (#!) handler functions
I like self-executing files, and sometimes these cause syntax errors when used or #included by other files.  Also, I like to put commonly used or default args on the #! line rather than entering them on the command line each time, so this handles those.

# exports
shebang(opts)
Text stream reader to comment out #! if found on first line.  Shebang event is optionally emitted.

options:
{
    emit: false, //whether or not to emit a "shebang" event into the stream
};


shebang_args(str)

Parse the #! line, return array of args found.  Parsing handles quotes, comments, whitespace or "#" within strings, etc.  (This turned out to be more challenging than I expected, so I made a reusable function)

#TBD
TODO: provide more info

#eof
