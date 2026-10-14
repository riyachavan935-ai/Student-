
🍔 SmartBite – Smart Food Ordering System

A Food Ordering Website with Verilog-Based Order Control Logic

SmartBite is a responsive food ordering website developed using HTML, CSS, and JavaScript. It allows users to explore food items, search by name, filter by category, add items to a shopping cart, calculate the total bill, and place demo orders.

The project also includes an IVerilog digital logic module that demonstrates order acceptance, food availability, order cancellation, and binary order status.

✨ Features

- Responsive and modern user interface
- Food menu with images, names, descriptions, and prices
- Search food items
- Filter by Burgers, Pizza, Desserts, and Drinks
- Add items to cart
- Increase or decrease item quantity
- Automatic subtotal, delivery fee, and total calculation
- Demo order placement and order status display
- Interactive Smart Order Controller
- Verilog module and testbench
- GTKWave waveform support

🛠️ Technologies Used

Technology| Purpose
HTML5| Website structure
CSS3| Styling and responsive layout
JavaScript| Menu, cart, billing, and UI logic
Verilog HDL| Digital order-control logic
IVerilog| Verilog compilation and simulation
GTKWave| Viewing simulation waveforms
GitHub Pages| Hosting the static website

📁 Project Structure

SmartBite-Food-Ordering/
│
├── index.html
├── style.css
├── script.js
├── food_order.v
├── food_order_tb.v
└── README.md

🚀 How to Run the Website

1. Clone or download this repository.
2. Keep "index.html", "style.css", and "script.js" in the same folder.
3. Open "index.html" in a web browser.

Run using GitHub Pages

1. Open the repository on GitHub.
2. Go to Settings → Pages.
3. Select Deploy from a branch.
4. Select branch "main" and folder "/(root)".
5. Click Save.
6. Open the published website using the URL provided in the Pages settings.

⚙️ How to Run the Verilog Simulation

Install Icarus Verilog on your computer. Open a terminal or CMD in the project folder and run:

iverilog -o food_sim food_order.v food_order_tb.v
vvp food_sim
gtkwave food_order.vcd

The first command compiles the Verilog module and testbench. The second runs the simulation and prints the output. The third opens the generated waveform in GTKWave.

🔌 Order Control Logic

The Verilog module uses three inputs:

Input| Description
"order_request"| Indicates whether an order is requested
"food_available"| Indicates whether the selected food is available
"cancel_order"| Indicates an order cancellation request

The module generates three outputs:

Output| Description
"order_accepted"| Indicates an accepted order
"order_cancelled"| Indicates a cancelled order
"order_status"| Two-bit binary order status

Order Status Table

Request| Available| Cancel| Accepted| Cancelled| Status
0| 1| 0| 0| 0| "00"
1| 1| 0| 1| 0| "01"
1| 0| 0| 0| 0| "00"
1| 1| 1| 0| 1| "11"

🧪 Testing

The testbench checks four scenarios:

1. No order request.
2. Order accepted when food is available.
3. Order not accepted when food is unavailable.
4. Order cancellation.

Simulation output can be viewed in the CMD terminal, and signal transitions can be inspected in GTKWave.

🎯 Project Objectives

- To develop a user-friendly food ordering website.
- To understand basic front-end web development.
- To implement digital logic using Verilog HDL.
- To verify the logic using a testbench and simulation.
- To demonstrate the relationship between a user interface and digital order-control concepts.

⚠️ Limitations

- This is an educational demonstration project.
- Orders are not stored permanently in a database.
- No real payment or online transaction is performed.
- GitHub Pages hosts the front end but does not compile or execute Verilog files.
- The website's interactive logic panel demonstrates the same basic rules in JavaScript; the Verilog module is simulated separately using IVerilog.

🔮 Future Enhancements

- User registration and login
- Database integration for persistent orders
- Admin dashboard and menu management
- Real-time order tracking
- Backend integration with a Verilog simulation service
- Secure payment gateway integration for a production version

👩‍💻 Conclusion

SmartBite combines a responsive food ordering interface with a Verilog-based digital order controller. It demonstrates web development, shopping cart operations, billing calculations, Boolean logic, and digital simulation in one educational project.

---

Project Name: SmartBite – Smart Food Ordering System
Project Type: Web Development + Digital Logic Simulation
Purpose: College Academic Project
Payment: Demo only — no real transactions
