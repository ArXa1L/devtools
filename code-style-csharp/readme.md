### Installation

Steps to install code style to a new project when using VS + ReSharper:

1. Add a dependency on 'vostok.devtools' to cement's module.yaml file.

2. Copy .editorconfig file to solution directory.

3. Copy [Solution].DotSettings file to solution directory and rename it to match .sln file.


There are several assumptions behind the choice of relative file paths:

1. Module's cement directory is located on the same level with vostok.devtools.

2. Solution file is located in the root of module directory.

If any of these are not true, you will need to adjust paths in .DotSettings file.

### Notes

Currently, our code style enforces the following file layout:

* All constants, in order: public, non-public.

* All fields, in order: public static, non-public static, public, non-public.

* Events.

* All constructors, in order: public static, non-public static, public, non-public.

* Finalizers.

* Grouped by access modifier: all public, all internal, all protected, all private:

    - static properties

    - static methods

    - properties

    - methods

    - indexers and operators

* Delegates.

* Enums, classes, structs, interfaces.