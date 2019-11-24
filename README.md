Overview
========
JAVA Hibernate ORM connection example

How-to run
==========
Requirements:

Java 8,
Gradle and
PostgreSQL 10.* or higher

Steps to run:

_1._ Set up database server. Download Postgres from https://www.postgresql.org/download/

_2._ Execute the following SQL in your Postgres database to create and set up postgres table:
```
CREATE TABLE public.employee
(
    id integer NOT NULL GENERATED ALWAYS AS IDENTITY ( INCREMENT 1 START 1 MINVALUE 1 MAXVALUE 99999999 CACHE 1 ),
    name character varying(20) COLLATE pg_catalog."default",
    role character varying(20) COLLATE pg_catalog."default",
    insert_time timestamp without time zone,
    CONSTRAINT employee_pkey PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE public.employee
    OWNER to postgres;
```

_3._ Change the database access credentials in hibernate.cfg.xml

_4._ Compile the project using gradle

_5._ Run the Main method

