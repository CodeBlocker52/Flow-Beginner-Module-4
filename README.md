# Flow-Beginner-Module-4


This Repo is made for an Assessments for the eth-avax Intermediate project for Metacrafters. The purpose of this Repository is to showcase my knowledge and understanding of the smart contracts and especially, about creating my own Tokens,with mentioned requirements.

Description
This Repository consists of a contract named function.sol written in Cadence, a programming language used for developing smart contracts on the Flow blockchain. 

## Getting Started
### Executing program
To run this program, you can use Flow Playboard at https://play.flow.com/


```cadence

 access(all) contract SomeContract {
    pub var testStruct: SomeStruct

    pub struct SomeStruct {

        //
        // 4 Variables
        //

        pub(set) var a: String

        pub var b: String

        access(contract) var c: String

        access(self) var d: String

        //
        // 3 Functions
        //

        pub fun publicFunc() {}

        access(contract) fun contractFunc() {}

        access(self) fun privateFunc() {}


        pub fun structFunc() {
            /**************/
            /*** AREA 1 ***/
            /**************/
            //variable read : a,b,c,d

            //variable write :a,b,c,d

            //function call:  publicfun,contarctfun,privatefun
            
        }

        init() {
            self.a = "a"
            self.b = "b"
            self.c = "c"
            self.d = "d"
        }
    }

    pub resource SomeResource {
        pub var e: Int

        pub fun resourceFunc() {
            /**************/
            /*** AREA 2 ***/
            /**************/
             //variable read :a,b,c

            //variable write :a

            //function call :  publicfun,contarctfun
        }

        init() {
            self.e = 17
        }
    }

    pub fun createSomeResource(): @SomeResource {
        return <- create SomeResource()
    }

    pub fun questsAreFun() {
        /**************/
        /*** AREA 3 ****/
        /**************/
            //variable read  :a,b,c

            //variable write :a

            //function call : publicfun,contarctfun
    }

    init() {
        self.testStruct = SomeStruct()
    }
}
```


This contract has commented out all access control all the variables i.e a , b , c, d and three functions i.e publicFunc , contractFunc and privateFunc .
Also, the access of these variables and functions inside the Script.cdc file is also provided.



## Authors
CodeBlocker52(https://github.com/CodeBlocker52 )

## License
This project is licensed under the MIT- see the LICENSE.md file for details
