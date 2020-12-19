

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
        <li><a href="#built-with">Patterns Used</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#covered-features">Covered Features</a></li>
    <li><a href="#uncovered-features">Uncovered Features</a></li>
  </ol>
</details>



## About The Project

First Version for Electronics Store E-Commerce System

### Built With

1. .Net Core v3.1
  * AutoMapper.Extensions.Microsoft.DependencyInjection v8.1.0
  * Microsoft.EntityFrameworkCore.SqlServer v3.1.10
  * Microsoft.EntityFrameworkCore.Tools v3.1.10
2. Angular CLI: v11.0.4 
3. Node: v14.15.1

### Patterns Used
  * Repository Pattern
  * Dependency Injection ( For follow Dependency Inversion Principle Of SOLID Design Prenciples)



## Getting Started

### Prerequisites

1. Visual Studio 2019 (Recommended)
2. Node.js v 14.15.1
3. PostMan (for API Testing)
4. Angular v 11.0.4 


### Installation

Database Used : Local DataBase (built in tool in Visual Studio 2019)

  For making a successful connection with database make sure that your local port is the same as the name under ```Default``` key under ```ConnectionStrings``` 
  key in ```appsettings.json``` under root folder named ```Electronics Shop WebAPI``` .

  This line is for DB connection
    ```  "Default": "server=localhost; database=ElectronicsShopDB; Integrated Security=True;" ```
  
Angular URL Port (Client API) : ```AngularUrl": "http://localhost:8080/```

WebAPI URL Port : ```http://localhost:8888```

So make sure that those two ports are free for use before **start** 

*in case you change the port for WebApi , you should add that URL in the ```Base``` file under **ClientAPP** folder* .


Steps to start Project:

1. Connect with your local Database via SQL Server
2. make sure that packages  **Microsoft.EntityFrameworkCore.SqlServer (3.1.10)** and **Microsoft.EntityFrameworkCore.Tools (3.1.10)** is installed under the root folder of Electronics   Shop WebAPI
3. Run those commands in the corresponding order to generate Database from Models (Code First Approach)
  
     ```
     Add-Migration DeployMigration
     ```
  
     ```
      Update-Database
      ```
  
4. Run Angular server from inside **ClientAPP** through this command
    ```
    ng serve --port 8080
    ```

5. you are ready to discover now :)


## Covered Features 

1. DataBase Design including ERD and Database Diagram (For Cient Side Cycle)

2. Forms including 
  *Login Form* 
  *Registration Form*
  
   These forms including :
     
   * strict validation on all mandatory fields from client side on: 
  
        * All columns using -> Reactive Forms ( supported by Angular ) except Birth Date column (doesn't have vaildaiton in UI but you can't submit vaildation form without enter the date of birt) .
      
   * validation from server side on : 
     
        * Checking if Email that was added is exist or not ( Registration Form )
        * Checking if User email is exist ( Login Form )
        * Checking if Password is correct , in condition of the email address is exist ( Login Form ) 

3. List ```All Products``` as Default Filteration  

4. **Filterations** by **Category** ```Laptops``` , ```TVs``` , ```Sound Systems```

5. **Pagination** with max **5** products

6. **APIs** For :

    **Categories :**
      
      * GetCategories
    
    **Products :**
      
      * GetProducts
      * GetProductsByCategory(For Product Filteration)
      * AddProduct (For Administration)
    
    **Customers:**
    
      * GetCustomers
      * GetCustomer (one single customer)
      * AddCustomer
      
  7. **PostMan APIs For Testing**    

## Uncovered Features 

1. Back-end pages for the administrators including :

      **Add products in client side**
    
      **Filter products in client side**
    
      **Discount Feature**
    
2. Quantity beside each product

3. Arabic Language is not supported

4. Disable any post back in filtering in both Products and buyer listing page

5. **APIs** For:

    **Orders**
    
      * GetOrders
      * AddOrder
      * UpdateOrder
      
6. Manual URL by customer ( you can enter module manually through URL ) .

7. Add Product button is disabled .
      
      

