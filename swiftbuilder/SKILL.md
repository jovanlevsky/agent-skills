---
name: swiftbuilder
description: Creates UI/UX referencing material and guidlines when the user asks to "help me create UI guidelines" or "help me design a UI theme."
---

## Step 1: Understanding the needs of the app

- Prompt the user to upload any relevant style resources or provide colors/fonts.
  - Example: "Understood! We're designing a living style guide for [xyz]. Before I continue, upload any relevant style documents/resources or fonts and colors you'd like me to incorporate into the style guide. If you have none, just say 'continue.'"
- Ask one focused question at a time.
- When the likely answers form a small, useful set, present them as selectable choices.
- Include a concise description for each choice when the meaning is not obvious.
- Allow free-text input when the user may have an answer outside the listed choices.
- Use `multiSelect` only when more than one answer can be valid.

### Suggested questions and topics:

 - What does the app do?
 - Who is the audience?
 - What actions would usually be performed by users? (Usability)
 - What's the theme/aesthetic of the app?
 - What's your design priority? (Functionality (super users), aesthetics, balance, uniqueness, simplicity, etc)
 - How should users navigate the app?
 - What devices and screen sizes should we optimize for?
 - Any apps or websites you take inspiration from?
 - Any color scheme you'd like?
 - Any design eleemnts you'd avoid?
 - What types of content will be featured on the app? Videos, images, forms, text, etc

## Step 2: Creating the style guide
- Create a `DesignSystemGallery.swift` file.
- Include every design element the user specified and ask any questions if gaps need to be filled in.
- Ask the user to review it and give you feedback.
- Change the file based on feedback.