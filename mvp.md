
# Reduced Test Build

The purpose of this reduced test build is to demonstrate the core value proposition of Matry.
A reduced test build is one step lower than a minimally viable product.
The idea is not to create a solution that is viable for customers; only to prove that the essential idea is sound.
In order to achieve this, we need to do the following:

1. Summarize the value proposition
2. List the minimal functionality required
3. Describe the system that could satisfy these requirements

## Value Proposition

Matry provides UI designers with a textual interface for describing the visual behavior of digital products.
Though it seems counter-intuitive, using text instead of images provides designers with far greater flexibility, expressiveness, and efficiency.

## Minimal Functionality

For Matry to be minimally viable, designers must be able to:

1. Define design resources by filepath
   1. Define custom fonts
   2. Define images
2. Define globally accessible design tokens
   1. Define named colors
   2. Define named numbers
   3. Define named text values
   4. Define named font assets
   5. Define named image assets
3. Define components
   1. Define custom name for a component
   2. Define input options for a component
      - number
      - font
      - text
      - boolean
      - font
      - image
   3. Define internal values for a component
   4. Define elements for a component
      - boundary
      - shape
      - text
      - image
   5. Nest elements for a component
   6. Style elements in a component
   7. Change an elements style given certain conditions
   8. Nest components
4. Define stories
   1. Define custom name for a story
   2. Define one or more frames for a story
   3. Define a single, existing component to be rendered in a frame
   4. Define the inputs for a component for a given frame
5. View output
   1. View list of stories
   2. View single story

## System Design

A system that could satisfy the above requirements would be:

- A node app that watches `.matry` files in a directory
- On application start, as well as on file change, parse tokens/components/stories within `{project name}/.src`
- On navigation to `/` show a list of tokens, components, and stories
- On click of a story, navigate to `/{story name}`
- On navigation to `/{story name}`, render the story
