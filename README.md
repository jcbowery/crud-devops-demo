# crud-devops-demo
testing this free tier pro devops tutorial

# Setup DB first
# Run SQL script on your DB
# Copy the SQL file into the container
docker cp infrastructure/db.sql postgres_crud_users:/db.sql

# Enter the container
docker exec -it postgres_crud_users psql -U postgres -d crud_users -f /db.sql

# Backend
cd backend
npm install
node index.js  # or npm start

# Frontend
cd ../frontend
npm install
npm start


