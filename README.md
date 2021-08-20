# Qt6 Book

The new home for the Qt6 book (based on QmlBook)

You can always find the latest version of the book built at [https://distracted-dijkstra-f5d508.netlify.app/](https://distracted-dijkstra-f5d508.netlify.app/).

# Contents

1. Building the Book Locally
2. For Reviewers
3. For Authors

# 1. Building the Book Locally

The contents is built into a static site using [VuePress](https://vuepress.vuejs.org/). The packages are managed ysing [Yarn](https://yarnpkg.com/).

To build the contents locally, run:

```
$ yarnpkg
$ yarnpkg run docs:dev
```

Then visit [localhost:8080](http://localhost:8080) to view the book.

To build the examples, run:

```
$ yarnpkg run examples:build
```

This will create the `_examples/` directory with the build. It assumes Qt6 can be found by CMake. My typical command line on a Debian Linux machine looks like this:

```
$ CMAKE_PREFIX_PATH=/path/to/Qt/6.2.0/gcc_64/lib/cmake/ yarnpkg run examples:build
```

Subsequent calls do not need `CMAKE_PREFIX_PATH` to be specified.

# 2. For Reviewers

Pick chapters to review from the [Project Board](https://github.com/qmlbook/qt6book/projects/1). Also look for issues tagged as [Questions](https://github.com/qmlbook/qt6book/issues?q=is%3Aissue+is%3Aopen+label%3Aquestion) in the project.

Reviews are welcome both as issues, or as pull requests. Pick the approach that is the easiest for you!

# 3. For Authors

Chapters are outlined in `docs/.vuepress/config.js`. Please tag chapters as `Qt5`, `Qt6 Draft`, and `Qt 6` respectively.
