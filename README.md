### For study eslint

Ref: 

	https://www.youtube.com/watch?v=nxxl2H_TOTc&list=PLMWjeRChIK6bnp6qaS3rxLGCpc9aQYzEE
    Check git log for steps to using eslint

Example:
	
    {
      "extends": "airbnb",
      "parserOptions": {
        "ecmaVersion": 6
      },
      "env": {
        "node": true,
        "es6": true,
        "browser": true
      },
      "rules": {
        "comma-dangle":["error", "never"],
        "no-unused-vars": ["error", 
          {
            "vars": "local",
            "args": "none"
          }
        ],
        "react/jsx-filename-extension": [1, {
          "extensions": [".js", ".jsx"]
        }]
      }
    }

1. Install eslint as a Dev dependence, .node_modules/.bin added in .bashrc
so can run local modules from current directory

2. Custom eslint config by extends eslint:recommended. extends work like inheritence in 
programming, with this we have all setting from eslint:recommended

3. Custom eslint to add parserOptions and env.
    - *parserOptions*: to config js version, here ecmascript version 6
    - *env*: to config execution environment which to has access to global variables on that environment like set *browser* env to has access to *document object*

4. Install eslint extension for VSCode, this extension expect two thing to work
  	- *eslint module* installed globally or locally (locally in this case)
  	- *.eslintrc* config file in project directory

5. Install eslint airbnb config and extends it

6. To customize eslint rules:
	- when using build-in rules: https://eslint.org/docs/rules/
    - When using eslint rules from plugin like react: google search for its name
