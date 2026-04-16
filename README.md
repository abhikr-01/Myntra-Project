🛍️ Myntra Clone
A full-stack e-commerce fashion web app inspired by Myntra — browse products, add them to your bag, and see a real-time price breakdown before checkout.
📌 Overview
This project is a clone of the popular Indian fashion e-commerce platform Myntra. It features a React + Vite frontend with Redux for state management, and a Node.js + Express backend that serves product data via a REST API.
Users can browse products on the Home page, add them to their Bag, and view a detailed price breakdown — all powered by a live backend.
✨ Features
🏠 Home Page — Fetches and displays products from the backend on load
👜 Bag Page — Shows all items added to the bag
➕ Add to Bag — Add any product from the Home page
❌ Remove from Bag — Remove items from the Bag
💰 Price Summary — Displays:
Original Price (total MRP)
Discount Applied
Convenience Fee
Final Payable Amount
⏳ Loading Spinner — Shown while products are being fetched
🔄 Redux State Management — Bag and fetch status managed via slices
🖥️ Pages
Page           File                          Description
Home      routes/Home.jsx      Product listing — fetches items from backend
Bag       routes/Bag.jsx       Selected items with live price summary
🛠️ Tech Stack
Frontend (Myntra-react-clone/)
        Technology                               Purpose
         React.js                               UI framework
         Vite                                Build tool & dev server
         Redux                               Global state management
         HTML5 / CSS3                        Structure & styling
         JavaScript                          Logic & interactivity
Backend (backend/)
       Technology                                 Purpose
         Node.js                                  Runtime
        Express.js                              REST API server
        items.json                              Product data source

📁 Project Structure

Myntra-Project/
│
├── Myntra-react-clone/          # React Frontend
│   ├── public/
│   │   ├── images/
│   │   ├── favicon.svg
│   │   └── icons.svg
│   ├── src/
│   │   ├── components/
│   │   │   ├── BagItem.jsx       # Individual bag item card
│   │   │   ├── BagSummary.jsx    # Price breakdown component
│   │   │   ├── FetchItems.jsx    # Fetches products from backend
│   │   │   ├── Footer.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── HomeItem.jsx      # Individual product card
│   │   │   └── LoadingSpinner.jsx
│   │   ├── routes/
│   │   │   ├── App.jsx           # Main app with routing
│   │   │   ├── Home.jsx          # Home page
│   │   │   └── Bag.jsx           # Bag page
│   │   ├── store/
│   │   │   ├── index.js          # Redux store setup
│   │   │   ├── bagSlice.js       # Add/remove bag logic
│   │   │   ├── itemsSlice.js     # Product items state
│   │   │   └── fetchStatusSlice.js  # Loading state
│   │   ├── index.css
│   │   └── main.jsx
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
│
├── backend/                      # Express Backend
│   ├── data/
│   │   └── items.js              # Product data module
│   ├── scripts/
│   │   ├── index.js
│   │   └── bag.js
│   ├── app.js                    # Express server entry point
│   ├── items.json                # Product JSON data
│   ├── bag.html / bag.css        # Static bag page
│   ├── index.html / index.css    # Static home page
│   └── package.json
│
└── README.md

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

