# NOTES: Full Stack Redux Tutorial

URL: http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html

## Important Notes:

1. NODE FIRST, REACT SECOND :D
2. Make clear separation between server & client

## Steps (in general)

1. Node (server application):
    - Initialize package.json
    - Install babel transpiler: babel-core, babel-cli, babel-preset-es2015
    - Install testing libraries (for test units): mocha, chai
        - mocha: test framework
        - chai: assertion/expectation library
    - Add test scripts into package.json: 
        - `"run": "mocha --compilers js:babel-core/register --recursive"`
            - Meaning: for running the mocha tests, transpile the tests first (ES2015 to ES5) and do the testing recursively (inside subdirs)
        - `"run:watch": "npm run test -- --watch"`
            - Meaning: mocha blablabla --watch (?), the lone double dash indicate end of options for the previous command.
            - More info: http://unix.stackexchange.com/questions/11376 what-does-double-dash-mean-also-known-as-bare-double-dash
    - Add babel preset into package.json:
        ```
        "babel": {
            "presets": ["es2015"]
        }
        ```
    - 