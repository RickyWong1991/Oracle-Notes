1. To Get Oracle enviroment language:
   select userenv('LANG') from dual
2. Decode：
   DECODE函数的语法是：
   decode( expression , search , result [, search , result]... [, default] )
   Sample：
     SELECT supplier_name,  
            decode(supplier_id, 10000, 'IBM',  
                   10001, 'Microsoft',  
                   10002, 'Hewlett Packard',  
                   'Gateway') result  
     FROM suppliers;  
  Explain Sample：
   IF supplier_id = 10000 THEN  
      result := 'IBM';  
  
   ELSIF supplier_id = 10001 THEN  
      result := 'Microsoft';  
  
   ELSIF supplier_id = 10002 THEN  
      result := 'Hewlett Packard';  
  
   ELSE  
      result := 'Gateway';  
  
   END IF; 
