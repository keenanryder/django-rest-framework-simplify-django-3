### 12/16/2022 1.5.0
[DJANGO UPGRADE]
- Upgraded for official `Django3.2` compatibility

### 12/6/2021 1.4.1
[PYTHON COMPATIBILITY]
- Upgraded compatibility: `python3.6`, `python3.7`, `python3.8`, and `python3.9` now supported
- (necessary) Dropped deprecated `pycrypto` library in favor of `pycryptodome`

### 12/6/2021 1.4.0
[DJANGO UPGRADE]
- Upgraded for official `Django2.2` compatibility
- Updated requirements for `pymongo` and allow for loose resolution for `djangorestframework`
	- this is necessary to continue to support `<python3.7`
- Valid for `python3.6` and `python3.7`

### 12/8/2020 1.3.26
Fixed nested relation lookup returns null instead of exception.

### 2/5/2020 1.3.24
Fixed `PostgresExecutorService` to not error working with a stored procedure without arguments.

### 7/29/2019 1.3.16
Fixed `SimplifyJsonTextField` custom Django field to prevent json.dumping() value more than once

### 7/29/2019 1.3.15
Added revicontains filter that will allow you to do an icontains but on the passed in filter against a database field. Note: currently does not work with lists


### 7/29/2019 1.3.14
Added `SimplifyJsonTextField` custom Django field which allows a non-json compatible database to handle json responsibly

### 12/18/2018 1.3.1
No changes just removing a few bad versions ;)

### 9/14/2018 1.2.5
psycopg2 updated to version 2.7.3 so verify compatability

### 8/16/2018 1.2.2
Added exclude functionality on included items to ensure they are never included by accident

### 5/15/2018 1.2.0
Added get_filterable_properties to the SimplifyModel which will allow you to filter based on a property that is on the model. Currently this is restricted to predefined values and cannot accept arguments to the filter at this time. Look at the PhaseGroup model and URL for examples.

### 5/6/2018 - 1.1.7
Added REQUEST_FIELDS_TO_SAVE to the SimplifyModel which will allow us to save fields from the request object directly to the SimplifyModel. This is a property that is set on the SimplifyModel and it is a list of tuples. For example if you wanted to save the "method" from the request onto a SimplyModel field of "verb" you would simply add the attribute REQUEST_FIELDS_TO_SAVE = [('method', 'verb')]
