# `Case 4` - Клиенты, сделавшие более пяти заказов - `Александра Бужор`

## Запрос SQL:
```
SELECT 
    Customers.CustomerID, 
    Customers.CustomerName, 
    COUNT(Orders.OrderID) AS NumberOfOrders, 
    MAX(Orders.OrderDate) AS LastOrderDate
FROM 
    Customers, Orders
WHERE 
    Customers.CustomerID = Orders.CustomerID
GROUP BY 
    Customers.CustomerID, 
    Customers.CustomerName
HAVING 
    COUNT(Orders.OrderID) > 5
ORDER BY 
    COUNT(Orders.OrderID) DESC;
```
## Результат:

![image](https://github.com/user-attachments/assets/a150a672-2a38-46bd-9d88-715676c52e8d)
