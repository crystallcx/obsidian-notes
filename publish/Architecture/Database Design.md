### Understanding the Building Blocks of a Web Application: Routes, Controllers, Services, Repositories, and Databases

> It's worth noting that the repositories interact with the database, not the controllers or services. This level of abstraction ensures that changes to the database structure or type affect only the repository layer and not the whole application.


# Services


# Repositories
- acts as an abstraction layer between the services and the DAL (data access layer)
- communicates directly with the database and encapsulates the logic required to access the database
- by adoption this seperation, we achieves more maintainability and scalability, making it easier to modify the database or switch  to a different database.
-```
```jsx
import { User } from '../models/User';

export class UserRepository {
    async getAllUsers(): Promise<User[]> {
        // Logic to fetch all users from database
    }

    async createUser(user: User): Promise<User> {
        // Logic to create a new user in database
    }

    async updateUser(user: User): Promise<User> {
        // Logic to update an existing user in database
    }
}
```