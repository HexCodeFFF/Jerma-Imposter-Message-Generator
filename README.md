![Improved jerma imposter message generator](sus!!!.png)

A modified version of
[aechaechaech's jerma imposter message generator](https://github.com/aechaechaech/Jerma-Imposter-Message-Generator)
which is used to cut and splice the popular jerma "When the imposter is sus!😳" meme into any message.

# usage

this version is designed to be used by other python scripts. the main function is `sus.sus()`. it takes a string (the
message) and returns the randomly generated filename of the output image. the filename is generated
using `sus.temp_file()` and by default outputs a png to the working directory, but this can be changed.

# changes

- lives in a function instead of a standalone file
- fixes issue where output image can be too big or too small due to assuming all letters are the same size
- input string is no longer case sensitive
- duplicate letters are chosen in a repeating pattern instead of randomly, this allows the original image to be
  reconstructed from the original text.
- modes are removed, always on non-cypher and cheat mode.
- chooses a random slice for any "cheat mode" letters ONCE, and uses the same slice for the same letter for the rest of
  the image.
- the size of "cheat mode" letters is determined based on the size of the letter, instead of a fixed size.

# but why though

I'm implementing this code into a discord bot i'm working on and i might as well publish the changes i made