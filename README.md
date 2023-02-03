# Naming Conventions
    Class Name - CapitalCase
    Property, Method - camelCase
    Variable Name, Database Name, Column Name, Table Name - snake_case
# Trait
    trait name
    use name
    different file - require/include
    Although traits were not allowed to declare constants, it was possible to access constants in PHP classes that the traits are used in.
    
    ```php
    class BaseClass {
      const CONSTANT = "Base class constant";
    }

    trait MyTrait {
      public function showConstant() {
        echo BaseClass::CONSTANT;
      }
    }

    class ChildClass extends BaseClass {
      use MyTrait;
    }

    $child = new ChildClass();
    $child->showConstant();  // Outputs: Base class constant
    ```
