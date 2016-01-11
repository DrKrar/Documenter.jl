<a id='Public%20Documentation-1'></a>

# Public Documentation

<a id='Lapidary.makedocs-1'></a>

<a href='#Lapidary.makedocs-1'> # </a>**Function**

```
makedocs(
    src    = "src",
    build  = "build",
    format = ".md",
    clean  = true
)
```

Converts markdown formatted template files found in `src` into `format`-formatted files in the `build` directory. Option `clean` will empty out the `build` directory prior to building new documentation.

`src` and `build` paths are set relative to the file from which `makedocs` is called. The standard directory setup for using `makedocs` is as follows:

```
docs/
    build/
    src/
    build.jl
```

where `build.jl` contains

```julia
using Lapidary

makedocs(
    # options...
)
```

Any non-markdown files found in the `src` directory are copied over to the `build` directory without change. Markdown files are those with the extension `.md` only.
<hr></hr>