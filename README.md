def is_year_leap(year):
    if year%4 != 0:
       return False
    elif year%100 != 0:
       return True 
    elif year%400 != 0:
       return False 
    else:
        return True
    
def days_in_month(year,month):
      month_days=[31,28,31,30,31,30,31,31,30,31,30,31]
      months1=["JANUARY","FEBRUARY","MARCH","APRIL","MAY","JUNE","JULY","AUGUST","SEPTEMBER","OCTOBER","NOVEMBER","DECEMBER"]
      month == months1
      for i in range(12):
        month_days[i]== months1[i] 
      res = month_days
      if  month not in months1:
            return None
      if month == 'FEBRUARY' and is_year_leap(year):
         res = 29
      return res
years=int(input("Type in a year:"))
months=input("Type in a month:")
days=int(input("Type in the days:"))
print(years,months,days,"->",end=" ")
result=days_in_month(years,months)
if days == result  :
    print("ACCURATE")
else:
    print("WRONG","\n",years,months,result)
  
#days_in_month(years,months)
   



