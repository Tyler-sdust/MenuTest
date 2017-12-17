# MenuTest
HomeWork
```java
package pro_1215_01;

import java.util.Scanner;

public class MenuTest {

	public static void main(String[] args) {
		int num,num1=0,num2=0;
		while(num1==0) {
		num=showLoginMenu();
		if(num==1) {
			while(num2==0) {
				num1=showMainMenu();
				if(num1==0) {
					break;
				}
				if(num1==1) {
					num2=showCustMenu();
				}
				if(num1==2) {
					num2=showSendGMenu();
				}
			}
		}
		if(num==2)
			break;
		}
	}
	public static int showLoginMenu() {
		Scanner in=new Scanner(System.in);
		int num=1;
		String name,passWord;
		while(num==1) {
			System.out.println("欢迎使用XX购物管理系统");
			System.out.println("\t1.登陆系统\n\t2.退出");
			System.out.println("*********************************************");
			System.out.print("请选择输入对应的数字：");
			num=in.nextInt();
			if(num==1) {
				System.out.print("请输入用户名");
				name=in.next();
				System.out.println("请输入密码");
				passWord=in.next();
				if(name.equals("sym")&&passWord.equals("123")) {
					System.out.println("@@ 登陆成功："+name+" @@");
					break;
				}
				else {
					System.out.println("@@您没有权限进入系统，请重新登陆。@@");
					continue;
				}
			}
			if(num==2)
				System.out.println("谢谢您的使用");
		}
		return num;
	}
	public static int showMainMenu() {
		Scanner in=new Scanner(System.in);
		int num;
		System.out.println("XX购物管理系统主菜单");
		System.out.println("**********************************************");
		System.out.println("\t1.客户信息管理\n\t2.真情回馈");
		System.out.println("**********************************************");
		System.out.print("请选择，输入对应的数字（输入0返回上一级菜单）：");
		num=in.nextInt();
		return num;
		
		
	}
	public static int showCustMenu() {
		Scanner in=new Scanner(System.in);
		int num=5;
		System.out.println("XX购物管理系统>客户信息管理");
		System.out.println("**********************************************");
		System.out.println("\t1.显示所有客户信息\n\t2.添加客户信息\n\t3.修改客户信息\n\t4.查询客户信息");
		System.out.println("**********************************************");
		while(num<0||num>4) {
			System.out.print("请选择，输入对应的数字（输入0返回上一级菜单）：");
			num=in.nextInt();
			switch(num) {
			case 0:
				break;
			case 1:
				System.out.println("执行显示所有客户信息");
				break;
			case 2:
				System.out.println("执行添加客户信息");
				break;
			case 3:
				System.out.println("执行修改客户信息");
				break;
			case 4:
				System.out.println("执行查询客户信息");
				break;
			default:
				System.out.println("输入有误");
				break;
			}
		}
		return num;
	}
	public static int showSendGMenu() {
		Scanner in=new Scanner(System.in);
		int num=4;
		System.out.println("XX购物管理系统>真情回馈");
		System.out.println("**********************************************");
		System.out.println("\t1.幸运大放送\n\t2.幸运抽奖\n\t3.生日问候");
		System.out.println("**********************************************");
		while(num<0||num>3) {
			System.out.print("请选择，输入对应的数字（输入0返回上一级菜单）：");
			num=in.nextInt();
			switch(num) {
			case 0:
				break;
			case 1:
				System.out.println("幸运大放送");
				break;
			case 2:
				System.out.println("幸运抽奖");
				break;
			case 3:
				System.out.println("生日问候");
				break;
			default:
				System.out.println("输入有误");
				break;
			}
		}
		return num;
	}
}

