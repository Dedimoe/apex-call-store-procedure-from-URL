# apex-call-store-procedure-from-URL
Oracle Apex call store procedure from URL

Create procedure:
```
connect scott
create or replace procedure tst is
begin
HTP.prn( 'Test ...' );
end;
/
```

Give grant:
```
grant execute on tst to apex_public_user;
grant execute on tst to public;
```

Call from browser:
```
http://192.168.1.2:8080/pls/apex/scott.tst
```

The output:
```
Test ...
```
