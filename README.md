# Bloggen

`bloggen` is a simple static site generator that uses content in markdown format to generate a blog.

## Usage

You can install it with:

`go install github.com/emanuelquerty/bloggen/cmd`

Once install is complete, create a directory/folder called `markdown` and add an `example.md` file with the following content in the following format:

```
Title: Interesting title
Description: Some description or preview of your post
Tags: amazing, great

## I will be rendered as <h2> element

I will be rendered as a <p> element and I can be

This is another paragraph and it's really just a text
```

Please ensure the `Title`, `Description` and `Tags` words are at the top of each file as shown in the example file above.

### Run and create your site

Once you have your `example.md` file in your `markdown` directory, these are the following options:

`bloggen create --from <path to markdown directory>`

Running the above command will create a directory build with all your html, and css files.

### Preview your site

You can also preview your site by running:

`bloggen preview --from <path to markdown directory>`

This will spin up a server running on port `3000`

Go to ` http://localhost:3000/` to access your local site

### Adding static assets

You can add images or videos in your `build/assets/img` folder and then reference them in your markdown. Really, the body of your `post` can contain any html content in markdown format such as bellow:

```
## Blogging from Your Wix Blog Dashboard

On the dashboard, you have everything you need to manage your blog in one place.

![I'm an image alt text ](../assets/img/some-image.jpeg)

## This is a subtitle h2 element

This is more paragraph ...

And so on
```

If you want to reference markdown syntax, you can use the excellent tutorial from one of the creators and start adding creating with `bloggen':

Reference: https://daringfireball.net/projects/markdown/syntax

## Running `bloggen` in development mode

If you just want to play with it with some posts already created, you can download the entire project so you can test it without installing it. There is a `Makefile` which contains `build` and `run` and `preview` proccesses.

You can build the executable with:

`make build`

Or create the site with:

`make create`

Or even preview it with:

`make preview`

This project is still in development but I hope it may be useful for you in any way. I plan on adding more features and make it easier to use. Feel free to add issues or open pull requests. Any help is welcome.
