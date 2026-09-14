# SQL Injection Notes

## Objective

To demonstrate SQL Injection in DVWA running in a controlled local lab environment.

## Payload 1

```sql
1' OR 1=1#
```

This payload modifies the SQL condition so that it always evaluates to true. The application returned multiple user records instead of only one record.

## Payload 2

```sql
1' OR 'a'='a'#
```

This payload uses a condition where 'a' is equal to 'a'. Therefore, the condition evaluates to true and multiple records may be displayed.

## Observed Result

The application displayed multiple user records, including usernames and other database information.

## Security Impact

- Unauthorized exposure of database records
- Bypassing normal search restrictions
- Possible authentication bypass
- Exposure of sensitive application information

## Prevention Methods

1. Use prepared statements and parameterized SQL queries.
2. Validate and sanitize user input.
3. Never directly concatenate user input into SQL queries.
4. Apply the principle of least privilege to database accounts.
5. Avoid displaying detailed database errors to users.
6. Perform regular security testing and code reviews.

## Ethical Note

Testing was performed only on the intentionally vulnerable DVWA application running locally for educational purposes.