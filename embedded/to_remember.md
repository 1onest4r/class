- c is pass by value meaning every variable has a copy and function only ever sees the copy of the variable and if we wish to access the actual value we use pointers
- crash is GOOD outcome compared to silent corruption
- ```
  printf() // doesn't actually just print
		   // so use (void *) for printing ptr
  ```
- always use  ``` (void *)``` to output address of things you are dealing with
- ``` *pv++ ``` if you do it inline the ==increment== happens after the destructing happens