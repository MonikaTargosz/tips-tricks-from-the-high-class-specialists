# Basic operations - the processes of constructing, copying, moving and destroying objects

[1] Design [constructors], [assignments] and [destructors] as sets of operations. 

[2] 5 cases where an object can be copied or moved: as an assignment source, object initialiser, function argument, function return value; 
or as an exception. 

[3] Assignment uses the copy or move operator. In other cases, a copy or move constructor is used. 

[4] [Constructors] are used to initialise named objects and objects in free memory, temporary objects and implement explicit type conversion. Defaults should be generated using the compiler. A class containing a [destructor] should have a user-defined or deleted copy and move operation.

[5] [Rule-zero] is to define all needed operations or none (using all defaults).

[6] Pre-define copy or forbid it (e.g. do not generate copy in the base class) with [=default] and [=delete], indicating that we do not want to generate the operation (function). 

[7] By default, declare unary constructors as [explicit]. 

[8] If a class member has [default-value] (used whenever the constructor does not provide another value), use it as [initialiser-of-member-data].

[9] [Copy] and [move] - Return containers by value using copy elision and move. Use const reference argument types for large operator arguments. 

[10] [Resource-management] - Manage all resources using the [RAII-method] (Resource Acquisition Is Initialization). A class that is a resource handle must have a user-defined constructor user-defined constructor, destructor and other than default copy operations.

[11] [Operator-overloading] If you overload an operator give it a standard meaning and define all cooperating operations. 

[12] [Standard-operations] If you define the <=> operator for a type as non-default, additionally define == .

Source: A Tour of C++ (C++ In-Depth Series), 3rd Edition - 2023 Pearson Education, Inc. 