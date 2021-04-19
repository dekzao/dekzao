```cs
using ERP24;

namespace ERP24.SoftwareDeveloper
{
  public class SoftwareDeveloper 
  {
    private string _name;
    private string _title;
    private string _company;
    private string _location;

    public string Name 
    {
      get { return _name; }
      set { _name = value; }
    }
  
    public string Title 
    {
      get { return _title; }
      set { _title = value; }
    }
   
    public string Company 
    {
      get { return _company; }
      set { _company = value; }
    }
  
    public string Location 
    {
      get { return _location; }
      set { _location = value; }
    }
  
    public SoftwareDeveloper(string name, string title, string company, string location)
    {
      Name = name;
      Title = title;
      Company = company;
      Location = location;
    }
  
    public virtual string getInfo()
    {
      return $"{Name} is a {Title} based in {Location} currently working for {Company}";
    }
  }
}
```


```cs
using System;
using ERP24.SoftwareDeveloper;

namespace ERP24.SoftwareDeveloper
{
  class Program 
  {
        static void Main(string[] args) 
        {
         var user = new SoftwareDeveloper("Pedro Soares", "Sofware Developer", "ERP24", "Porto");
         Console.WriteLine(user.getInfo());
         Console.ReadLine();
        }
  }
}
```
