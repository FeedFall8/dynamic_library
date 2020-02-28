-------------introduction---------
hello there! dynamic script is a intrpreted langauge but a very special one
dynamic scripts syntax is based on python dictionarys dynamic also has special keywords,characters and abilitys to enable you to develop full fledged applications!
games and more can be developed in dynamic script so lets dive in to coding
-----setup-----------
it is recommended to follow the three steps...
1. have python installed for full capabilitys such as packaging
2.set all files with the extension: " .dynamic" to always open with dynamic_library.exe
3.set all files with .func to open with notepad
4.read on :)
------------a dynamic hello world------------------
{ #all scrips MUST BEGIN WITH A {
    system.cout('hello world')
}
`------------------------------------------------------
congrats you did your first hello world in dynamic script! lets move into variable defining,importing and much more
-------------defining variables------------------
to define a variable we will use a special keyword called "#>var>" in dynamic this is called a command key
example:
{
 #>var>string = "hello" #you can also include a commet too :)
}
------------package importing----------
time to REALLY make dynamic script useful package importing now exists! but theres requirements....
-dynamic at the moment only supports python packaging
-python 37-32BIT MUST be installed to package! if you do not want to do this it is recommended to change the system.path variable to your current pythons version site packages folder
-local packages such as packages in same dir of script are acceptable
-packages may not entirely work if they are not 37-32
anyways lets package!
example:
{
   #import>pygame
   #e>import CPP #and this is a commet
    #import>SDLLIB as sdl #impossibru!!!!

}
and for those wanting to import a specific class or function..
{
    system._from(Package,function) #package is the module to import from, function is the class or obj to import from that module
   or if we want to add more directorys to import files from...:
   system.new_path(<path>)
}

but say you dont want to install 37-32 python well you can now link directorys! to where your packages are which areusually somwhere in appdata/program folder on win10
example of package linking

{
	system.new_path(pathtositelibs)
}#packages linked gg!

but if you still are expiriencing issues time to brute force link it!
{
	sys.path.append(yourpathname) 
}
make sure path names are spelled correct! and readable
heres a last ditch effort if theres STILL issues be exact!:
{
	#e>sys.path = [],
	#e>sys.path = ['',"C:\\Users\\FeedFall8\\AppData\\Local\\Programs\\Python\\Python38-32\\lib\\site-packages"]
	print(sys.path),
	#import>pygame
} #this should HARD WIRE the sys path to find your package
----------trouble shooting-----------
coding ENITRELY in dictionarys can have its ups and downs so we added a way to run python code in mid or any part of the program
to run code in the middle of a program example:
{
 #e>print('hi') #executing a line of python code is useful as it #e> always run FIRST and defines FIRST before dynamics main code is ran
}
-----adding functions------
{
	#>func_source>this.func #implements stuff :)
}
.func files syntax example: this.func texts..:
print('ive been initalized!')
def func():
    pass

---deleteing STUFF IS FUN HEHEHEHEHE--------
to delete a variable,item,function or ruin everything! do ~ at the beginning of anything :) it will delete it
note:  use #e> del(var or item) to delete stuff as ~ may NOT work and youll have a ghost variable :)
--------looping--------------
examples:
{
 #e>system.loop('''while True: print('hi'); print('why'); #we use ; to say newline rather than indent :)''') #recommended to use 3 qoutes
}
----commets-----
in dynamic theres 2 keywords with # a norm commet(#) and a command(#>) 
if you run a command you can commet using  a basic # after the command
do NOT double ## or you will get a crash/error
--------system class functions and abiltys------
the system class is VERY useful especially for controlling flow of packages,code and more dont go overtwriting the system class or youl have issues
systems classes and functions:

system.cout(text) -> text output
(more soon)
---errors--
if you need to see errors in your script click on dynamic to open the console or do cd then dynamic_lib.exe(dependng on what its named')
inside of the console type this.. to see errors:
C:\Users\FeedFall8\Desktop\dynamiclibrary>errors_on - enables  the errors to be shown
C:\Users\FeedFall8\Desktop\dynamiclibrary>errors_off - dissable erros immediate window close!
--commands--
#e> - used to run a simple line of python code. usually to brute force code. this can be multiple lines using ; after each code word like...: #e>cout('hello');cout("world");. this command can also be used to OVERWRITE dynamics basic functions which is NOT recommended
#>var> - defines a variable example: #>var>hello = "hi"
#import> - used to import a python package (will support dynamic script importing soon!)
#>func_source> - adds functions or defines them using the .func file format
#noah> - sets the amount of specified data to be flooded
#arkholding> - sets the data type to be flooded with (default is 0)
#flood> - floods a variable with specified data example: [0,0,0,0,0,0](return value and permanent value)
----defining commands----
you can define commands by placing your cmd name in the "command_plugins" folder :) 
all commands are callable by the file name for instance if you have add.json in the folder the command #>add> will be added
all commands must have a main function inside of the file 
example of function structure:
def main(arg): #all commands will receive a tuple argument so be prepared
    print(arg[0])#reference the WHOLE tuple
    print(arg[0][0])#print the first element of the argument

---------------
remember all arguments will be tuple its recommended to use arg[0] to get the values
also if you need to see the the tuple itself do #>checkarg>(values) this will give the tuple value and you can easily use this to help you structure yout function

-----system modules----
json - used for json handling
system.sock - used for network handling
system.sys - the sys of the system
sys - the system
system.math - extra pre done math methods
system.req - used for handling simple url checking ect
system.sos - the system os - WIN 10 ONLY linux ehh
system.byte - serializes objects
(these modules will expand if you link python packages)
-----system self functions-----
system.cout - outputs a simple string into the console system.cout('hello 8)') ---> hello 8)
system.print() - prints an indefinite number of strings ..( system.print('hi','jhon') ---> hijhon)
system._exit() - shuts the program down!

more soon!