Food Delivery and Payment Integration System

A Java-based console application demonstrating the integration of structural design patterns. This project simulates a food ordering platform where customers can customize their meals with dynamic add-ons and complete their purchases using various third-party payment gateways.

Developed as a 2nd Laboratory Activity for Integrative Programming.

Core Structural Patterns Implemented

Decorator Pattern (src/decorator/): Used to dynamically attach add-on services (e.g., Extra Cheese, Extra Sauce, Priority Delivery) to base food items without modifying existing class structures. This prevents class explosion (avoiding classes like BurgerWithCheeseAndSauce) by layering features at runtime.

Adapter Pattern (src/payment/): Used to bridge incompatible third-party payment interfaces (PayPal's makePayment(), GCash's sendMoney(), and Maya's transferFunds()) into a unified PaymentProcessor interface with a standardized pay() method.

Features & Business Rules

Dynamic Order Customization: Base meals (Burger, Pizza, Chicken Meal) can be customized with multiple add-ons. Descriptions and prices are aggregated automatically.

Minimum Order Validation: The system rejects transactions where the final order cost is strictly below P100.00.

Tiered Add-on Qualification: Priority Delivery (P50.00) can only be attached to orders if the current subtotal has reached at least P200.00.

Payment Validation: Prevents processing for zero or negative payment amounts.

Customer Profiling: Captures and displays the customer's name, contact number, and delivery address on the final receipt.

Project Structure
Plaintext
src/
├── food/
│   ├── FoodOrder.java
│   ├── Burger.java
│   ├── Pizza.java
│   └── ChickenMeal.java
├── decorator/
│   ├── FoodOrderDecorator.java
│   ├── ExtraCheese.java
│   ├── ExtraSauce.java
│   ├── LargeDrink.java
│   └── PriorityDelivery.java
├── payment/
│   ├── PaymentProcessor.java
│   ├── PayPal.java
│   ├── GCash.java
│   ├── Maya.java
│   ├── PayPalAdapter.java
│   ├── GCashAdapter.java
│   └── MayaAdapter.java
└── order/
    ├── Order.java
    └── Main.java



How to Run?


1. Ensure you have the Java Development Kit (JDK 17 or higher) installed.

2. Compile the classes from the root src directory:

Bash
javac order/Main.java


3. Execute the main program:

Bash
java order.Main

4. Follow the interactive console prompts to input customer details, select food, apply decorators, and process the adapted payment.


Author
Reyjoy Peñanueva Sabino

3rd Year, BS Information Technology - Mobile System Development

Davao Oriental State University

Integrative Programming Laboratory