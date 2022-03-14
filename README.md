# inheritance
import java.util.*;
class employee
{
int id;
String name,designation;
Scanner k=new Scanner(System.in);
void reademp()
{
name=k.next();
designation=k.next();
id=k.nextInt();
}
class salary extends employee
{
int BP,HRA,DA,PF,NP;
Scanner k=new Scanner(System.in);
void readsal()
{
BP=k.nextInt();
HRA=k.nextInt();
DA=k.nextInt();
PF=k.nextInt();
}
void calculate_salary()
{
NP=BP+HRA+DA-PF;
System.out.println("the net pay is"+NP);
}
void dispemp()
{
System.out.println("name of the employee is"+name);
System.out.println("designation is "+designation);
System.out.println("id no is "+id);
System.out.println("the net pay is "+NP);
}
}
class Main
{
public static void main(String args[])
{
Scanner k=new Scanner(System.in);
System.out.println("enter the value of n");
int n=k.nextInt();
int i;
employee e=new employee();
salary s= new salary();
for(i=0;i<n;i++)
{
s.reademp();
s.readsal();
s.calculate_salary();
s.dispemp();
}
}
}
}


