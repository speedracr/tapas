# Ruby tapas

## Character literals
To check if a single character was entered, preceed it with a '?'. Ex.
`if ?y puts "Proceeding..."`

## %W quoting - ep. 5
Elements of an array that is preceeded by %W quoting can be turned into
string elements without having to worry about white spaces. Ex.
`recording_options = %W[-f 960x600 -r]` will turn into `"-f 960x600 -r"`
when used in a system command like `system "ffmpeg", *recording_options`

Advantage of %W vs. %w: interpolation is possible.
````
width = 960
height = 600

recording_options = %W[-f #{width}x#{height} -r]
````
