# py-carbon [![Badge](https://img.shields.io/pypi/v/py-carbon?color=3776AB&logo=python&style=for-the-badge)](https://pypi.org/project/py-carbon/)  [![Badge 2](https://img.shields.io/pypi/dm/py-carbon?color=3776AB&logo=python&style=for-the-badge)](https://pypi.org/project/py-carbon/)
Fully asynchronous Python library for [carbon.now.sh](https://carbon.now.sh)

## Installation
```
$ pip install py-carbon
```

## A quick example
In this example we'll create a carbon image and save it to disk.
```py
import carbon
import asyncio

code = """
defmodule Something do
    def anything() do
        IO.puts "Hello, World"
    end
end
"""  # Any kind of code-block in any language


async def main():
    cb = carbon.Carbon()  # Create a Carbon instance
    opts = carbon.CarbonOptions(code=code)  # Set the options for the image
    image = await cb.generate(opts)  # Generate the image
    await image.save('hello')  # Save the image in png format


asyncio.run(main())
```

And it'll output something like this:  
  
<img src="https://github.com/itsmewulf/py-carbon/blob/main/examples/something-script.png?raw=true" alt="Carbon Image" width="400"/>

### Contributing
This package is opensource so anyone with adequate python experience can contribute to this project!

### Reporting Issues
If you find any error/bug/mistake with the package or in the code feel free to create an issue and report
it [here.](https://github.com/itsmewulf/py-carbon/issues)

### Fixing/Editing Content
If you want to contribute to this package, fork the repository, make your changes and then simply create a Pull Request!

### Contact
If you want to contact me:  
**Mail -** ```paul@przybyszew.ski```  
**Discord -** [wulf](https://dsc.bio/wulf)
