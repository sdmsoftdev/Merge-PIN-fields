# Merge-PIN-fields
Merge PIN field with OtherPIN to create one column for PINs in the same table


Update [My_Table]
set Column1 = Column2 
where pin ='' 

go

Update [My_Table]
set Column1 = Column2 
WHERE CHARINDEX('.',Column2) = 0 AND CHARINDEX(',',Column2) = 0       
AND ISNUMERIC(Column2) = 1 and LEN (Column2) >= 11 and Column1 = ''
