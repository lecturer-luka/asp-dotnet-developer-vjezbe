<div align="center">

<!-- title -->

# Osnovne vježbe za klase uzorka repozitorija i sučelja u web aplikaciji ASP.NET MVC

<!-- description -->

Skup vježbi pokriva najosnovnije načine mogućih klasa modela sa svojstvima, klasa kontrolera s radnjama, klasa repozitorija i naziva pogleda za web aplikacije koje koriste uzorak repozitorija u C#.

</div>


## Vježba 1

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Vježba je stvoriti jednostavnu "CRUD" web aplikaciju kozmetičke trgovine korištenjem uzorka repozitorija u C#.
3. Kreirajte klase modela:
	* Customer
		* Id (int)
        * Name (string)
        * Email (string)
        * Phone (string)
        * Address (string)

    * Product
        * Id (int)
        * Name (string)
        * Description (string)
        * Price (decimal)

    * Order
        * Id (int)
        * OrderDate (DateTime)
        * TotalAmount (decimal)
        * CustomerId (int)

    * OrderItem
        * Id (int)
        * Quantity (int)
        * ProductId (int)
        * OrderId (int)

4. Kreirajte klase kontrolera:
    * CustomerController
        * Index()
        * Create()
        * Edit(int id)
        * Edit(int id, Customer customer)
        * Delete(int id)
        * DeleteConfirmed(int id)

    * ProductController
        * Index()
        * Create()
        * Edit(int id)
        * Edit(int id, Product product)
        * Delete(int id)
        * DeleteConfirmed(int id)

    * OrderController
        * Index()
        * Create()
        * Edit(int id)
        * Edit(int id, Order order)
        * Delete(int id)
        * DeleteConfirmed(int id)

5. Kreirajte sučelja za klase repozitorija:
    * ICustomerRepository
        * IEnumerable<Customer> GetCustomers()
        * Customer GetCustomerById(int id)
        * void AddCustomer(Customer customer)
        * void UpdateCustomer(Customer customer)
        * void DeleteCustomer(int id)

    * IProductRepository
        * IEnumerable<Product> GetProducts()
        * Product GetProductById(int id)
        * void AddProduct(Product product)
        * void UpdateProduct(Product product)
        * void DeleteProduct(int id)

    * IOrderRepository
        * IEnumerable<Order> GetOrders()
        * Order GetOrderById(int id)
        * void AddOrder(Order order)
        * void UpdateOrder(Order order)
        * void DeleteOrder(int id)
        * IEnumerable<OrderItem> GetOrderItemsByOrderId(int orderId)
        * void AddOrderItem(OrderItem orderItem)
6. Stvorite klase repozitorija koje nasljeđuju gornja sučelja.
7. Stvori poglede:
    * Customer
        * Index.cshtml
        * Create.cshtml
        * Edit.cshtml
        * Delete.cshtml

    * Product
        * Index.cshtml
        * Create.cshtml
        * Edit.cshtml
        * Delete.cshtml

    * Order
        * Index.cshtml
        * Create.cshtml
        * Edit.cshtml
        * Delete.cshtml
        * OrderItems.cshtml
8. Na temelju danih prijedloga izradite funkcionalnu web aplikaciju koja će podatke spremati u memoriju ili vanjsku ".json" datoteku.
     > Entity Framework bit će pokriven u modulu 8.
