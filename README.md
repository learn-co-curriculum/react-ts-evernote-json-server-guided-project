# Phase 2 Guided Project Guidelines

We've learned a lot, congratulations on making it this far! React and TypeScript
can be difficult topics to digest. It takes time and practice, and that's what
you'll be doing in this guided project.

To practice what we've learned, you'll be building an Evernote-like application
with React. Additionally, your application should be written in TypeScript - so
don't forget about typing!

Your goal will be to complete the baseline deliverables using the provided
starter code and then make this project your own by building out unique stretch
goals. Some suggestions are listed below, but feel free to be creative and think
of your own!

## Requirements

- Complete all of the deliverables
- Build out at least 1 stretch goal feature

## Setup

The project provides the backend JSON Server API code for you in `src/db`, and
has starter code for the React frontend in `src/components`. The latter is where
you will be doing all your work.

To get started, fork and clone this repository, then:

1. Setup and run your frontend with `npm install && npm start`. This React app
   will be running on `http://localhost:4000`.
1. Seed your json-server database with `npm run seed`.
   - This will seed some starter data for you in the `db/db.json` file. Any time
     you want to reset your database to its original state, just run
     `npm run seed` again to overwrite your data with some fresh seed data.
1. Start the server with `npm run server`. This backend API will be running on
   `http://localhost:3000`.

### User ID

The seed file should create one user for you, so your default `userId` should be
`1`. You can check the `db/db.json` file to make sure.

#### Routes

| Method | Route        |                               Headers                               |        Body         |
| ------ | ------------ | :-----------------------------------------------------------------: | :-----------------: |
| GET    | `/users`     |                                                                     |                     |
| GET    | `/notes`     |                                                                     |                     |
| POST   | `/notes`     | `'Content-Type': 'application/json'`;`'Accept': 'application/json'` | title, body, userId |
| PATCH  | `/notes/:id` | `'Content-Type': 'application/json'`;`'Accept': 'application/json'` | title, body, userId |

**Bonus Tip:**

- Test out your routes with [Postman](https://www.getpostman.com/) to see how
  they work and what they return.

## Provided Code

- All CSS styles are provided for you.
- The JSON Server API is provided for you.
- Many components are provided for you, but most are not completely functional.
  It is your job to read the code and figure out how to incorporate it into your
  app.

## Deliverables

Look at the gif below to see how the app should look and behave. These are the
baseline deliverables you need to complete:

### Viewing and Displaying Notes

- [ ] Display all notes in the left sidebar.
- [ ] Displayed sidebar notes should show the title and a truncated body.
- [ ] When a note from the sidebar is clicked, display its contents in the right
      panel.

![completed display notes](https://curriculum-content.s3.amazonaws.com/phase-2/react-hooks-evernote-json-server-guided-project/react-evernote-display.gif)

### Filtering Notes

- [ ] Implement the filter to search through your notes list by title.

![completed filter notes](https://curriculum-content.s3.amazonaws.com/phase-2/react-hooks-evernote-json-server-guided-project/react-evernote-filter.gif)

### Creating Notes

- [ ] At the bottom of your left sidebar, show a `New` button.
- [ ] Clicking `New` will create a new note via a `POST` request with some
      default title and body. **NOTE**: You don't have to use any kind of
      `<form>` element for this deliverable; you can create an object with a
      default title and body text when the button is clicked. Make sure to check
      the [Routes](#Routes) section of this README to determine what data you
      need in the body of your request.
- [ ] This new note should appear in the sidebar.

![completed create notes](https://curriculum-content.s3.amazonaws.com/phase-2/react-hooks-evernote-json-server-guided-project/react-evernote-create.gif)

### Editing Notes

- [ ] When displaying a note in the right panel, show an `Edit` button.
- [ ] Clicking the `Edit` button will allow the user to edit the title and body
      in the right panel.
- [ ] When in edit mode, also show a `Save` button which saves the note via a
      `PATCH` request.
- [ ] When in edit mode, also show a `Cancel` button which discards any changes
      and reverts back to displaying the note.
- [ ] Clicking a different note while in edit mode should discard your changes
      and display the new note instead.

![completed edit notes](https://curriculum-content.s3.amazonaws.com/phase-2/react-hooks-evernote-json-server-guided-project/react-evernote-edit.gif)

## Stretch Goals

When you are finished with the _deliverables_, you can build out any new
features that you want. This is your chance to be creative and make your project
unique!

Some suggestions:

- Add the ability to filter by body, date created, date edited, etc.
- Sorting by date created, date edited, alphabetical, etc.
- Use `react-router` to create a multi-page app
- User signup & login
- Sharing notes with other users
- Rich text formatting
- Tagging
- Emailing notes

To pass this project, you need to add at least **one extra feature** that was
not outlined in the required deliverables. You are free to use any of the
suggestions above, or come up with your own!

## Submission

Once you've completed your project, be sure to submit the link to your forked
repository on Canvas and give yourself a pat on the back!
