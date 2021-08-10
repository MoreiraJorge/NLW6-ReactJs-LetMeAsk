<p align="center">
  <img alt="Letmeask" src="src/assets/images/logo.svg" width="160px">
</p>

<p align="center">
  <img src="https://img.shields.io/static/v1?label=NLW&message=06&color=8257E5&labelColor=000000" alt="NLW Together 06" />

  <img  src="https://img.shields.io/static/v1?label=license&message=MIT&color=8257E5&labelColor=000000" alt="License">   
</p>

<h1 align="center">
    <img alt="Letmeask" src="src/assets/images/cover.svg" />
</h1>

<br>

## 🧪 Frameworks / Techs

This project was developed using the following frameworks / techs:

- [React](https://reactjs.org)
- [Firebase](https://firebase.google.com/)
- [TypeScript](https://www.typescriptlang.org/)

## 🚀 How to run this project

Clone the project and go into the directory.

```bash
$ git clone https://github.com/MoreiraJorge/NLW6-ReactJs-LetMeAsk.git
$ cd NLW6-ReactJs-LetMeAsk
```

To start this project, follow the steps:
```bash
# Install dependencies
$ yarn

# Run the project
$ yarn start
```
The app will be running in the following address: http://localhost:3000.

> It is necessary to create an account in [Firebase](https://firebase.google.com/) and a project with Realtime Database enabled.
> Here is a set of rules that you can use:
> ```
>  {
>   "rules": {
>     ".read": false,
>     ".write": "auth != null",
>     "$roomId": {
>       ".read": true,
>       ".write": "auth != null && (!data.exists() || data.child('authorId').val() == auth.id)",
>       "questions": {
>          ".read": true,
>          ".write": "auth != null && (!data.exists() || data.parent().child('authorId').val() == auth.id)",
>          "likes": {
>            ".read": true,
>            ".write": "auth != null && (!data.exists() || data.child('authorId').val() == auth.id)"  
>          }
>       }
>     }
>   }
>  }
> ```
> ### This project was also deployed with firebaste hosting: https://letmeask-eeac5.web.app/

## 💻 Project

Letmeask is perfect for content creators to create Q&A rooms with their public to answer questions, in an organized way. 

This project was developed during **[Next Level Week Together](https://nextlevelweek.com/)**, from the 20th to 27th of June 2021.


## 🔖 Layout

You can visualize the layout in the link bellow:

- [Web Layout](https://www.figma.com/file/u0BQK8rCf2KgzcukdRRCWh/Letmeask/duplicate) 

Remeber that you need a [Figma](http://figma.com/) account.

---

Many thanks to Rocketseat 👋🏻