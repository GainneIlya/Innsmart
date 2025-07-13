# `Case 4` - Клиенты, сделавшие более пяти заказов - `Трофимов Илья`

## Запрос SQL:
```
SELECT Customers.CustomerID, 
       ContactName, 
       COUNT(OrderID), 
       MAX(OrderDate)
FROM Orders
LEFT JOIN Customers ON Customers.CustomerID = Orders.CustomerID
GROUP BY Customers.CustomerID, ContactName
HAVING COUNT(OrderID) > 5
ORDER BY COUNT(OrderID) DESC;
```
