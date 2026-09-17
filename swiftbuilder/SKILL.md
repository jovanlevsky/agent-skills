---
name: swiftbuilder
description: Creates UI/UX referencing material and guidlines when the user asks to "help me create UI guidelines," "help me design a UI theme," or to "help me create a design for a page." Can also be invoked by the planner skill.
---


## Step 1: Understanding the needs of the app

- Prompt the user to upload any relevant style resources or provide colors/fonts.
  - If the user invokes this skill when asking for a style guide or the planner skill invokes it for a full app design:
  - Example: "Understood! We're designing a living style guide for [xyz]. Before I continue, upload any relevant style documents/resources or fonts and colors you'd like me to incorporate into the style guide. If you have none, just say 'continue.'"
  - If this skill is invoked by the user to design a specific page or wireframe, or the planner skill invokes it for a specific design:
  - Example: "Understood! We're designing a page or feature. Before I continue, upload any relevant style documents/resources or fonts and colors you'd like me to incorporate into the page or feature. If you have none, just say 'continue.'"
- Ask one focused question at a time.
- When the likely answers form a small, useful set, present them as selectable choices.
- Include a concise description for each choice when the meaning is not obvious.
- Allow free-text input when the user may have an answer outside the listed choices.
- Use `multiSelect` only when more than one answer can be valid.

### Suggested questions and topics:

 - What does the app/page/feature do?
 - Who is the audience?
 - What actions would usually be performed by users in this app or on this page? (Usability)
 - What's the theme/aesthetic of the app/page?
 - What's your design priority? (Functionality (super users), aesthetics, balance, uniqueness, simplicity, etc)
 - How should users navigate the app/page?
 - What devices and screen sizes should we optimize for?
 - Any apps or websites you take inspiration from?
 - Any color scheme you'd like?
 - Any design eleemnts you'd avoid?
 - What types of content will be featured on the app/page? Videos, images, forms, text, etc

## Step 2a: Creating the style guide
- Use this step if a style guide is being created.
- Create a `DesignSystemGallery.swift` file.
- Include every design element the user specified and ask any questions if gaps need to be filled in.
- Ask the user to review it and give you feedback.
- Change the file based on feedback.

## Step 2b: Creating the wireframe
- Use this step if a specific page or feature is being created and not an entire style guide.
- Create a `wireframe-[feature-name].swift` file.
- Include every design element the user specified and ask any questions if gaps need to be filled in.
- Ask the user to review it and give you feedback.
- Change the file based on feedback.