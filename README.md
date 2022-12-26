## Base Widget and View Templates

This Visual Studio Code extension provides templates for creating a `BaseWidget` and a `BaseView` in a Flutter project.

## Installation

To install the extension, follow these steps:

   <ol>
    <li>Download the latest <a href="https://www.google.com/">release</a>  to your computer</li>
    <li>Open vscode extensions</li>
    <li>Install from VSIX</li>
    <li>Select VSIX file and install</li>
  </ol>

## Usage

To use the templates, type the prefix for the desired template and press `Tab`. The prefixes for the templates are:

- bw for the BaseWidget template
- bv for the BaseView template

The templates use placeholders, which you can navigate through using the `Tab` key.

##Available Templates

- <h5>Crate Base Widget</h5>
  - Prefix: `bw`

  The `BaseWidget` template is used to create a widget that extends the `BaseWidget` class and takes two type arguments: `$2Cubit` and `$2State`. It has a single required constructor, which takes a key parameter and passes it to the `BaseWidget` constructor. The `build` method should be implemented to return a `Widget` that represents the visual representation of the widget.

    <h6>Here is the template:</h6>

  ```
    class $1Widget extends BaseWidget<$2Cubit, $2State> {
      const $1Widget ({super.key});

      @override
      Widget build(BuildContext context, $2Cubit cubit, $2State state) {
        return Container();
      }
    }
  ```

- <h5>Crate Base View</h5>

  The `BaseView` template is used to create a view that extends the `BaseView` class and takes two type arguments: `$2Cubit` and `$2State`. It has a single required constructor, which takes a key parameter and passes it to the BaseView constructor. The BaseView also expects a Cubit instance to be passed in its constructor, which is provided through the `$2Cubit.new` expression.

    <h6>Here is the template:</h6>

  ```
    class $1View extends BaseView<$2Cubit, $2State> {
      const  $1View({super.key}) : super(cubit: $2Cubit.new);

      @override
      Widget loadingBuilder(BuildContext context) {
        // TODO: implement loadingBuilder
        // NOTE: If there is no custom loading, default loading is used
        // If there is no custom loading, you can delete this block
        throw UnimplementedError();
      }

      @override
      Widget loadedBuilder(BuildContext context) {
        // TODO: implement loadedBuilder
        return Container()$0;
      }

      @override
      Widget? errorBuilder(BuildContext context, Object error) {
        // TODO: implement errorBuilder
        // NOTE: If there is no custom error, default error is used
        // If there is no custom error, you can delete this block
        throw UnimplementedError();
      }
    }
  ```

## For more information

- [Visual Studio Code's Markdown Support](http://code.visualstudio.com/docs/languages/markdown)
- [Markdown Syntax Reference](https://help.github.com/articles/markdown-basics/)

**Enjoy!**
