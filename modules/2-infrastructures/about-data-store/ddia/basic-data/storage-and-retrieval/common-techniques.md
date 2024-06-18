# Common Techniques

## (Redo) Log

1. For any in-memory data structure, we can append a record of the operation to a log file. In case of a crash, we can replay the log to restore the data structure.
