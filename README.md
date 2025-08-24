# markdown-lorem-ipsum

This is a GitHub repository whose profile contains markdown elements and text to use for testing whether markdown rendering is accessible or not.  The content and markdown elements are based upon the `light` and `dark` styles of [`charmbracelet/glamour` module](https://github.com/charmbracelet/glamour).

**Headers**

First, we have the markdown variants:

# markdown h1

## markdown h2

### markdown h3

#### markdown h4

##### markdown h5

###### markdown h6


**Horizontal Rule**

First, we have the markdown variants:

---


**Images**

First, we have the markdown variants:

![Animated image of a cat playing bongos](https://github.com/user-attachments/assets/a9931645-5f9b-4ccc-bf4b-52390b00c4a7)

![](https://github.com/user-attachments/assets/a9931645-5f9b-4ccc-bf4b-52390b00c4a7)


**Links**

First, we have the markdown variants:

[this is pure text](http://example.com)

[![Animated image of a cat playing bongos](https://github.com/user-attachments/assets/a9931645-5f9b-4ccc-bf4b-52390b00c4a7)](http://example.com)

[![](https://github.com/user-attachments/assets/a9931645-5f9b-4ccc-bf4b-52390b00c4a7)](http://example.com)

**Code**

First, we have the markdown variants:

`gh api "/user"`

```shell
QUERY='
query($endCursor: String){
  organization(login:"actions"){
    repositories(first:100, after:$endCursor){
      pageInfo{
        endCursor
        hasNextPage
      }
      nodes{
        name
        issues(states:OPEN){
          totalCount
        }
      }
    }
  }
}
'

gh api graphql -F query="$QUERY" --paginate --slurp | jq '[ .[].data.organization.repositories.nodes[].issues.totalCount ] | add'
```

```
this is just a code fence without a language applied.

this really shouldn't do anything exciting from a rendering perspective
```


**Quotes**

> [!NOTE]
> Duplicating markdown code blocks in HTML is not completely possible because GitHub HTML rendering would strip the necessary CSS styles to colorize specific text.
>
> In this example from [`andyfeller/gh-montage`](https://github.com/andyfeller/gh-montage), the help usage code block is rendered with special `span` elements and classes to highlight meaningful tokens in the markdown for `shell` use case:
>
> ```html
> <pre>$ gh montage --help
>
> Generate montage from GitHub user avatars.
>
> USAGE
>   gh montage [options] <span class="pl-k">&lt;</span>organization<span class="pl-k">&gt;</span>
>   gh montage [options] <span class="pl-k">&lt;</span>organization<span class="pl-k">&gt;</span>/<span class="pl-k">&lt;</span>team<span class="pl-k">&gt;</span>
>   gh montage [options] <span class="pl-k">&lt;</span>path/to/username file<span class="pl-k">&gt;</span>
>
> FLAGS
>   -a, --avatar-pixels <span class="pl-k">&lt;</span>integer<span class="pl-k">&gt;</span>       Size of GitHub avatar icons <span class="pl-k">in</span> pixels<span class="pl-k">;</span> default <span class="pl-s"><span class="pl-pds">'</span>48<span class="pl-pds">'</span></span>
>   -d, --debug                         Enable debugging
>   -f, --force                         Whether to overwrite output file <span class="pl-k">if</span> it exists
>   -h, --help                          Displays <span class="pl-c1">help</span> usage
>   -m, --montage-width <span class="pl-k">&lt;</span>integer<span class="pl-k">&gt;</span>       Width of GitHub montage <span class="pl-k">in</span> number of avatar icons<span class="pl-k">;</span> default <span class="pl-s"><span class="pl-pds">'</span>58<span class="pl-pds">'</span></span>
>   -o, --output-file <span class="pl-k">&lt;</span>output-file<span class="pl-k">&gt;</span>     Name of GitHub montage file to generate, without <span class="pl-s"><span class="pl-pds">'</span>.jpg<span class="pl-pds">'</span></span> extension
>   -p, --preserve                      Preserve temporary directory containing data</pre>
> ```


**Tables**

| Avatar | Name | Role | Handle
| ------ | ---- | ---- | ------
| ![@williammartin](https://avatars.githubusercontent.com/williammartin?s=80) | William | Engineering | [@williammartin](https://github.com/williammartin)
| ![@andyfeller](https://avatars.githubusercontent.com/andyfeller?s=80) | Andy | Engineering | [@andyfeller](https://github.com/andyfeller)
| ![@mxie](https://avatars.githubusercontent.com/mxie?s=80) | Melissa | Engineering | [@mxie](https://github.com/mxie)
| ![@jtmcg](https://avatars.githubusercontent.com/jtmcg?s=80) | Tyler | Engineering | [@jtmcg](https://github.com/jtmcg)
| ![@bagtoad](https://avatars.githubusercontent.com/bagtoad?s=80) | Kynan | Engineering | [@bagtoad](https://github.com/bagtoad)
| ![@ryanhecht](https://avatars.githubusercontent.com/ryanhecht?s=80) | Ryan | Product | [@ryanhecht](https://github.com/ryanhecht)

