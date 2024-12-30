# Contribution Guidelines for Proto Repo

Welcome to the Proto Repo of Epistemic Me. This is where we typically ideate on new features to introduce into Epistemic Me - prior to making any code changes. We believe that good data models and interfaces are what drive good architecture, and try to put data model ideation as early into the development of new features as possible. 

## Getting Started

### Fork and Clone
Begin by forking the repository to your own GitHub account, then clone it locally to start making changes.

### Environment Setup
Before you begin contributing to the Proto Repo, it's important to ensure that your development environment is properly set up. Follow these steps to configure your environment:

1. **Install Required Tools**: Make sure you have all the necessary tools installed to work with protobuf files. This includes the protobuf compiler (`protoc`) if not already installed, and any other specific dependencies listed in our `README.md`.
2. **Recommended IDE**: Any version of Visual Studio Code will work for editing and updating proto files. However, we recommend using **Cursor** for its enhanced features, including its LLM integrations, which help us move faster in our development processes. If you do not have Cursor, you can download it from [Cursor's official website](https://www.cursor.com/download).
3. **Configure Your IDE**: After installing Cursor, configure it to recognize the project's structure:
   - Open Cursor and navigate to 'File' > 'Open Workspace'.
   - Select the directory where you cloned the proto repo.
   - Ensure that Cursor's protobuf plugins or extensions are enabled and configured to highlight syntax and provide language support.

## Making Contributions

### Create an Issue
Before making any changes, check if there is an existing issue that matches the change you want to make. If there isn't one, create a new issue to describe the proposed features or enhancements. This coordination helps prevent duplicate efforts and allows for community input before you begin.

### Branching
Create a new branch from the main branch for your contributions. Use descriptive names like `feature/add-user-model` or `fix/user-model-typo` to reflect the nature of your changes.

### Define Data Models
- Modify or add new protobuf definitions as needed. Ensure that new fields are optional or have default values to maintain backward compatibility.
- We currently rely on using GitSubmodules to version changes to Proto files, we expect that updates to the Proto library also incur the responsibility of updating any official consumers: currenlty the Typescript and Server repos.
- Clearly comment on your changes within the models to explain their purpose and usage.

### Add Examples
Provide practical examples of how the proto files work by placing them in the `proto/examples` directory. This inclusion helps others understand and implement the models properly.

### Documentation
Update the `README.md` and other relevant documentation to reflect the nature of the changes. Include new model usage and any modifications in the examples directory.

## Submitting Changes

### Pull Request (PR)
After committing your changes locally, push your branch to GitHub and open a pull request against the main branch. Ensure your PR clearly describes the changes and includes references to any related issues.

### Code Review
Request reviews from project maintainers or other contributors. Make necessary revisions based on the feedback to align with the project's standards and integration needs.

## Updating Related Repositories Using Git Submodules

1. **Pull Latest Changes**: Once your PR is merged, update your local main branch in the proto repo and pull the latest changes:
2. **Update Submodule Reference**: In the root directory of any dependent repositories (like the TypeScript SDK or Server backend), update the proto submodule:
3. **Test and Push Changes**: Ensure the updates do not break any existing functionality by running tests or builds. Push these changes:
4. 4. **Pull Requests for Parent Repos**: Open pull requests in the parent repositories to merge the submodule updates, linking back to the proto repo changes.
5. **Review and Merge**: These updates require review. Notify maintainers to ensure a thorough check and integration.

## Community and Support

- **Discussions and Questions**: For any queries or support, use the GitHub Discussion feature or our community chat channels.
- **Stay Updated**: Keep an eye on the repository by watching it for new issues, PRs, and discussions.

Thank you for contributing to our project! By adhering to these guidelines, you help maintain the quality and consistency necessary for our software's reliability and scalability.
