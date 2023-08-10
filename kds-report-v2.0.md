# KDS Report 2.0

The new version of the KDS report will include a json schema, which defines it clearly.

The new version will allow 2 types of query.
A count query and a year query.

A count query is a query which counts the number of overall resources of a type or profile.
A year query is a query which counts the number of overall resources per year of a type of profile for all years since 2000 in yearly steps.

The following regex describes the allowed urls that can be used as part of the report input-queries:
```
^(((?!=)|_profile=|type=|date=eq[0-9]{4}(?![-])).)*_summary=count
```

## Counting queries

A count query can be identified by ending wit _summary=count.
Further the other allowed params should be 

## Counting for year queries

The counting for year queries will begin in the year 2000 and only counts of date parameters are allowed which use the eq comparator and are restricted to the year.

## Counting Encounter (Fall) instead of patient

It is to be discussed whether it is enough to count the Encounters per year or whether the Patients have to be counted.
If the patients have to be counted per year all encounters have to be downloaded and a unique count of all the patient ids referenced by the encounter has to be created.

## Time taken

It still has to be discussed whether the time a query has taken should be included.

