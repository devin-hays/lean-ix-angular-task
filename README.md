# LEANIX Angular Coding Challenge

# What you will be building:

You will build a web application using Angular that allows users to provide a personal API token (link to docs) to then be able to browse public GitHub repositories sorted by star count in descending order. When selecting a repository, they are navigated to a detail page that displays additional information about the repository and contains a list of its issues sorted by creation date descending.

## Summary of the requirements for your “GitHub Issue Explorer”:

Below these text requirements, we have also prepared a simple overview mockup showcasing the rough shape of each route you should implement.

Implements three routes using the Angular Router:

/: on the entry route, the user is presented with a form to input their GitHub
 API token. This token is required to access any of the other routes. Point the user to

this link for learning how to generate a token. Hint: for listing public repositories and their issues the token does not need to have any additional permissions that can be configured in the “New Personal Access Token”
 form.

/repositories: on this route the user is presented with a list of public GitHub repositories sorted by star count. Each list item should at least
 contain the info about the repository owner, name, and total stargazers. You may include additional information from the GraphQL API as you see fit. Below the list is a pagination component to display the results of the next or previous page. The pagination
 state is not to be persisted in the route state. By clicking on a list item, the user navigates to the route described below.

Warning: it is not about listing the public repositories that belong to the user who owns the provided token, but all public repositories on GitHub. This still requires a token.

/:owner/:repositoryName: on this route the user is presented with a detailed view of a public repository. Display whatever information you see fit
 about the repository on this page. You need to include a list of the issues of the repository sorted by creation date descending. Below the list is a pagination component to display the results of the next or previous page. The pagination state is not to be
 persisted in the route state.


Verifies that the provided API token is valid before navigating to the repository list using a test request to the GitHub GraphQL API.

If the test request returns an error in the response, you should display a meaningful error message next to the input element.

The user can jump back to the entry route by clicking on a “Change API token” link in the top right of the two sub-routes. By submitting the form again, they can change the token that the Angular application is using as a Bearer token for the GraphQL requests for the current session.

The API token is not persisted in anything like localStorage. Upon doing a full page reload, the user needs to enter their API token anew.

Use the latest version of the Angular CLI to create your angular project (npx -p @angular/cli ng new leanix-assignment). Use any stylesheet format you prefer. We use SCSS at LeanIX.

We have prepared some mockups that present the requirements of this assignment in one image. You may change the layout of the views as you like, as long as the required contents described above are included. Links to documentation of the GitHub GraphQL API:


The GitHub GraphQL API supports many different queries. The entire functionality of this assignment can be implemented using exactly two of those. If your implementation happens to use more than two, that is also fine.

Here is a list of pages you’ll definitely find helpful (most things you’ll need to find in there on your own):

Main entrypoint to the GraphQL API documentation:
https://docs.github.com/en/graphql 

Forming calls with GraphQL:
https://docs.github.com/en/graphql/guides/forming-calls-with-graphql

List of supported queries:
https://docs.github.com/en/graphql/reference/queries

Things we are looking for in your implementation:

- How you leverage TypeScript.
- Being able to answer questions about a third-party technology by reading the documentation and googling (in this case you will need to do this for the GitHub GraphQL API).
- Using rxjs Observables.
- Using the Angular Router.
- Using the Angular ReactiveFormsModule (API Token form).
- Consuming a GraphQL API (we are also heavily using GraphQL at LeanIX).
- User Experience.
- HTML Knowledge.

You are not required to add unit tests for your components or services. However, this might be a topic during the live interview. So testing some logic or interactions in your implementation beforehand can be useful.

Things we are not looking for in your implementation:

- Building the most beautiful interface ever seen. Feel free to use component libraries like Angular Material or even just native HTML elements with minimum styling.
- Multi-language support.

### Frequently Asked Questions:

Question:
May I use other libraries aside from the Angular framework for implementing the assignment?

Answer: 
Yes you may use any npm package that helps you build the assignmentin a way that makes sense to you.

Question:
What should I do when I have doubts about the requirements or I get stuck?

Answer: Reply to this E-Mail if you get stuck and we’ll help to unblock you.
