# Recipes Website

<img width="800" height="450" alt="1" src="https://github.com/user-attachments/assets/41448fe0-bb45-4278-a32d-6052aa45f36d" />

<img width="800" height="450" alt="2" src="https://github.com/user-attachments/assets/392443a1-6fea-4648-ae7b-45bda3a0e44e" />

[Live Demo](https://recipes-website.fedsg2007.workers.dev/)

## Screenshots

### Landing page

<img width="1916" height="955" alt="image" src="https://github.com/user-attachments/assets/570d299d-b868-43f1-94c4-524a945ea64c" />

<img width="1918" height="899" alt="image" src="https://github.com/user-attachments/assets/50367d30-00c3-4676-8272-1eefce3a3665" />

### Recipes filter

<img width="1916" height="368" alt="image" src="https://github.com/user-attachments/assets/09872a70-4d72-4cd0-abf1-04a3c611c970" />

### Bookmarks

<img width="1919" height="897" alt="image" src="https://github.com/user-attachments/assets/52dc61b3-18d3-422e-8aa2-725e3bd9ca57" />

### Registration/Authentication

<img width="438" height="537" alt="image" src="https://github.com/user-attachments/assets/d9bce871-1923-4dda-9530-3ed5f242ff51" />

<img width="409" height="437" alt="image" src="https://github.com/user-attachments/assets/0b0d1d88-03b8-4aa0-b3aa-8fe5bc9598d4" />

## Features

- Website containing variety of recipes for cooking
- Advanced filter: Find recipes by: category, difficulty, cuisine, dietary tags: cooking time
- Sort recipes by rating, cooking time or alphabetically
- Rate existing recipes and leave comments
- Add recipes to your bookmarks
- Create your own recipes
- Send your recipe on a review for it to become public for everyone

## How to use
1. Use Header or Footer to select type of recipe you want. Optionally hover over **Categories**, then press **All recipes** to show list of all recipes
2. Press button **Filters** to show filter menu. Choose preferred options, after that you can close the menu. Press **Reset all** at the right to reset filter options
3. Click on preferred recipe to show its page. Scroll down to see all the information, including servings, ingredients, steps and user reviews(if there are any)
4. Optionally you can rate the recipe by choosing 1-5 stars or/and leaving the comment
5. For more options, such as recipe making/bookmarks you need to register your account. At the top right corner press **Sign up** and make an account. After that in the top right corner press button with your username and press **Bookmarks**/**My recipes**
6. To create your recipe press **Add recipe** in **My recipes**, follow the instructions and fill up the fields. To add individual ingredients/steps press **Add** after each one. When you're done press **Review** to check how your recipe will look like and press **Add to your recipes** to save it
7. When checking your own recipe you have the options to **Delete**, **Edit** or **Publish** your recipe

## Tech Stack

**Frontend:** React/Nextjs, CSS(for variables), Tailwind, Vite, <br>
**Backend:** Node.js, Express, Socket.IO <br>
**Database:** PostgreSQL <br>
**Auth:** JWT (access + refresh tokens) <br>
**Hosting:** Cloudflare Workers (frontend, backend)

## How It Works

The database is the source of truth. When someone creates or changes a recipe, the website sends the request to the backend. The backend checks the recipe details and makes sure the user is allowed to make the change before saving it to the database. Recipe pages show the saved data, so visitors see the same recipe.
Published recipes are sent to a moderator for review. Once approved, your changes go live on the public recipe. You’ll be notified of the outcome either way.

## Getting Started

### Prerequisites

- Node.js 22 or newer
- A PostgreSQL database

### Installation

1. Clone the repo
   `git clone https://github.com/Yoribob/Recipes-Website.git`
2. Install dependencies in both folders
   `cd backend && npm install`
   `cd ../frontend && npm install`
3. Copy the environment files and fill in your values
   `cp backend/.env.example backend/.env`
   `cp frontend/.env.example frontend/.env.local`
   Set `DATABASE_URL` in `backend/.env` to your PostgreSQL connection string.
4. From the backend folder, apply the database migrations
   `npm run db:migrate`
5. Start the backend and frontend in separate terminals
   From the `backend` folder: `npm run dev`
   From the `frontend` folder: `npm run dev`

## Future Improvements

- Add images to all official recipes (user-submitted recipes excluded)
- Upgrade hosting to allow faster recipe loading
- Develop a more reliable way to ensure the quality of recipes

## AI Usage
AI tools were used during development for:

- Creating some recipes and sourcing images (Gemini API)
- Debugging during late-stage development, mainly deployment
- Drafting portions of the **Privacy Policy** and **Terms of Service**

AI-generated recipes can be inaccurate as not every recipe was review

## Credits

Some recipe data and photos are provided by [TheMealDB](https://www.themealdb.com/).

The app architecture, frontend, backend, database, and recipe features were designed and implemented by me.

## License

This project is licensed under CC BY-NC-SA 4.0. See [LICENSE](LICENSE) for details.
