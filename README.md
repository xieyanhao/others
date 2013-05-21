others
======

about abstract

/*
开发一个系统需要对员工进行建模，员工包含3个属性：姓名·工号·工资。
经理也是员工，除了含有员工的属性外，另外还有一个奖金属性。请使用
继承的思想设计出员工类和经理类。要求类中提供必要的方法进行属性访问。
*/

abstract class Employer
{
  private String name;
	private String id;
	private double pay;

	Employer(String name,String id,double pay)
	{
		this.name = name;
		this.id = id;
		this.pay = pay;
	}
	/*
	public class printName()
	{
		String a = "1";
		String b = "2";
		this.a = a;
	}
	public class aaa()
	{
		print this.a;
	}
	*/
	public abstract void work();
}

class Manager extends Employer
{
	private int bonus;
	Manager(String name,String id,double pay,int bonus)
	{
		super(name,id,pay);
		this.bonus = bonus;
	}
	public void work()
	{
		System.out.println("manage work");
	}
}
class  Employee
{
	public static void main(String[] args) 
	{
		String name = "1";
		String id = "2";
		double pay = 3.3;
		int bonus = 4;
		Manager m = new Manager(name, id, pay, bonus);
		m.work();
		System.out.println("Hello World!");
	}
}
