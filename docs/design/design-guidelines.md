---
title: Extension design guidelines
description: Docker extension design
keywords: Docker, extensions, design
---

# Design Guidelines

At Docker, we aim to build tools that integrate into a user's existing workflows rather than requiring them to adopt new ones. To that end, we strongly recommend that you follow these guidelines when building extensions. We will be reviewing and approving your Marketplace publication based on these requirements.

## Build a consistent experience with Docker Desktop.

Use the [Docker Material UI Theme](https://www.npmjs.com/package/@docker/docker-mui-theme) and the [Docker Extensions Styleguide](https://www.figma.com/file/U7pLWfEf6IQKUHLhdateBI/Docker-Design-Guidelines?node-id=1%3A28771) to ensure that your extension feels like it is part of Docker Desktop to create a seamless experience for users.

- Ensure the extension has both a light and dark theme. Using the components and styles as per the Docker style guide ensures that your extension meets the [level AA accessibility standard.](https://www.w3.org/WAI/WCAG2AA-Conformance)

![light and dark mode](./images/light_dark_mode.png){:height="50%" width="50%"}

- Ensure that your extension icon is visible both in light and dark mode.

![icon colors](./images/icon_colors.png)

- Ensure that the navigational behaviour is consistent with the rest of Docker Desktop. Add a header to set the context for the extension.

![header](./images/header.png){:height="50%" width="50%"}

- The advantage we have with Docker Desktop over the CLI is that we have the opportunity to provide rich information to users. Make use of this interface as much as possible. Avoid embedding terminal windows.

![terminal window](./images/terminal_window.png){:height="75%" width="75%"}

## Build Features Natively

- In order not to disrupt the flow of users, avoid scenarios where the user has to navigate outside Docker Desktop, to the CLI or a webpage for example, in order to carry out certain functionalities. Instead, build features that are native to Docker Desktop.

![switch context](./images/switch_context.png){:height="75%" width="75%"}

## Break Down Complicated User Flows

- If a flow is too complicated or the concept is abstract, break down the flow into multiple steps with one simple call-to-action in each step. This helps when onboarding novice users to your extension

![complicated flow](./images/complicated_flows.png){:height="50%" width="50%"}

- Where there are multiple call-to-actions, ensure you use the primary (filled button style) and secondary buttons (outline button style) to convey the importance of each action.

![call to action](./images/cta.png){:height="50%" width="50%"}

## Onboarding New Users

When building your extension, ensure that first time users of the extension and your product can understand its value-add and adopt it easily. Ensure you include contextual help within the extension.

- Ensure that all necessary information is added to the extensions Marketplace as well as the extensions detail page. This should include:
  - Screenshots of the extension.
  - A detailed description that covers what the purpose of the extension is, who would find it useful and how it works.
  - Link to necessary resources such as documentation.
- If your extension has particularly complex functionality, add a demo or video to the start page. This helps onboard a first time user quickly.

![start page](./images/start_page.png){:height="25%" width="25%"}
