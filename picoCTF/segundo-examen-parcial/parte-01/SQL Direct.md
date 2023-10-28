# SQL Direct
## Objetivo
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 56644 -U postgres pico`Password is `postgres`
## Solución
```
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 56644 -U postgres pico
Password for user postgres: 
psql (15.3 (Debian 15.3-0+deb12u1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \l
                                                List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    | ICU Locale | Locale Provider |   Access privileges   
-----------+----------+----------+------------+------------+------------+-----------------+-----------------------
 pico      | postgres | UTF8     | en_US.utf8 | en_US.utf8 |            | libc            | 
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 |            | libc            | 
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 |            | libc            | =c/postgres          +
           |          |          |            |            |            |                 | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 |            | libc            | =c/postgres          +
           |          |          |            |            |            |                 | postgres=CTc/postgres
(4 rows)

pico=# \d flags
                        Table "public.flags"
  Column   |          Type          | Collation | Nullable | Default 
-----------+------------------------+-----------+----------+---------
 id        | integer                |           | not null | 
 firstname | character varying(255) |           |          | 
 lastname  | character varying(255) |           |          | 
 address   | character varying(255) |           |          | 
Indexes:
    "flags_pkey" PRIMARY KEY, btree (id)

pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
```
## Notas adicionales
## Referencias