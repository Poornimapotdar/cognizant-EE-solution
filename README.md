Account datails:
//Implement code here
using System;
public class Account
{
privateint id;
private string accountType;
private double balance;

publicint Id
    {
get{ return id;}
set{ id = value;}
    }

public string AccountType
    {
get{ return accountType;}
set{accountType = value;}
    }
public double Balance
    {
get{ return balance;}
set{ balance = value;}
    }
public Account(){}
public Account(int id, string accountType, double balance)
    {
        this.id = id;
this.accountType = accountType;
this.balance = balance;
    }

publicboolWithDraw(double amount)
    {
if(balance>amount)
        {
balance -= amount;
return true;
        }
return false;
    }
public string GetDetails()
    {
return ("Account Id: " + id + "\nAccount Type: " + accountType + "\nBalance: "+balance);
    }
}
public class Program
{
static void Main(string[] args)
    {
        Account ac = new Account();

Console.WriteLine("Enter account id");
int id = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Enter account type");
stringaccountType = Console.ReadLine();

Console.WriteLine("Enter account balance");
double balance = double.Parse(Console.ReadLine());

Console.WriteLine("Enter amount to withdraw");
double amount = double.Parse(Console.ReadLine());

ac = new Account(id, accountType, balance);
Console.WriteLine(ac.GetDetails());

if(ac.WithDraw(amount))
        {
Console.WriteLine("New Balance: " + ac.Balance);
        }
    }
}
