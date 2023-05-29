This repository contains an instrumented go-lachesis-client that can produce substates for the first 4.5M blocks. 
To create a substate database, please issue the following command,
```
	./build/lachesis import events <lachesis-events>
```
While importing the evnent file, the substate.lachesis database is produced.
