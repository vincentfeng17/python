# python

sql table name

import sqlite3
import os  
conn = sqlite3.connect(os.path.join('data',"data.db"))
cursor = conn.execute('SELECT name FROM sqlite_master WHERE type = "table"')

      
table_names = [t[0] for t in list(cursor)]
print(table_names)
