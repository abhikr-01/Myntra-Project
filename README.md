Myntra Clone
A full-stack e-commerce fashion web app inspired by Myntra — browse products, add them to your bag, and see a real-time price breakdown before checkout.

Overview:

This project is a clone of the popular Indian fashion e-commerce platform Myntra. It features a React + Vite frontend with Redux for state management, and a Node.js + Express backend that serves product data via a REST API.
Users can browse products on the Home page, add them to their Bag, and view a detailed price breakdown — all powered by a live backend.

Features.
1. Home Page, fetches and displays products from the backend on load.
2. Bag Page, Shows all items added to the bag.
3. Add to Bag, Add any product from the Home page.
4. Remove from Bag, Remove items from the Bag.
5. Price Summary, Displays: Original Price (total MRP), Discount Applied, Convenience Fee, Final Payable Amount.

Loading Spinner is shown while products are being fetched. Redux State Management used in Bag, fetchs and status managed via slices.
* Pages                       
1. Home      routes/Home.jsx   for   Product listing — fetches items from backend
2. Bag       routes/Bag.jsx  has     Selected items with live price summary

🛠️ Tech Stack:
* Frontend (Myntra-react-clone): 
         React.js      for                         UI framework
         Vite      for                          Build tool & dev server
         Redux      for                         Global state management
         HTML5 / CSS3     for                   Structure & styling
         JavaScript        for                  Logic & interactivity
* Backend (backend/): 
         Node.js               for                   Runtime
        Express.js             for                 REST API server
        items.json            for                  Product data source

🚀 Getting Started
Prerequisites
Node.js (v16 or above)
npm
1. Clone the Repository
Bash
git clone https://github.com/abhikr-01/Myntra-Project.git
2. Run the Backend
Bash
cd backend
npm install
node app.js
The Express server will start and serve product data from items.json via API.
3. Run the Frontend
Bash
cd Myntra-react-clone
npm install
npm run dev
The React app will run at http://localhost:5173 (Vite default)

🔗 How It Works
1. When the Home page loads, FetchItems.jsx calls the Express backend API.
2. The backend reads from items.json and returns product data.
3. Products are stored in Redux (itemsSlice) and displayed via HomeItem.jsx.
4. A LoadingSpinner is shown while data is being fetched (fetchStatusSlice).
5. Clicking "Add to Bag" dispatches an action to bagSlice.
6. The Bag page reads from the Redux store and renders BagItem.jsx cards.
7. BagSummary.jsx calculates and displays the final price breakdown.

*Screenshots:
<img width="500" height="300" alt="Screenshot 2026-04-16 124937" src="https://github.com/user-attachments/assets/b7213c90-23a9-4977-a6d6-f6052b0dc06e" />
<img width="500" height="300" alt="Screenshot 2026-04-16 default" src="https://github.com/user-attachments/assets/58c51054-7f5f-4f6d-ac72-23441e2f4496" />
<img width="500" height="300" alt="Screenshot 2026-04-16 addtobag" src="https://github.com/user-attachments/assets/b8e6fd41-5ad0-4c5a-9433-44abcaac5e62" />
<img width="500" height="300" alt="Screenshot 2026-04-16 bag" src="https://github.com/user-attachments/assets/664d6d87-2aff-4dc4-ac40-874b72b443e7" />



