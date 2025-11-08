# suppergowhere
It's a side quest to build a web app that recommends places to go when the city is sleeping. 


SETUP INSTRUCTIONS:

Frontend
```
cd frontend
npm install
npm run dev
```

Type this onto the terminal to first install dependencies, and run the development server.


Backend
```
cd backend
go mod tidy      
go mod download   
go run .           
```

What this does is first tidy up the dependencies that are not being used. Then it downloads the dependencies required for the project. go run . basically means npm start but in golang terminology.