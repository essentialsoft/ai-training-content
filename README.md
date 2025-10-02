# ai-training-content

## Overview
This repository contains a collection of training materials and resources focused on AI and software development. The content is designed to help developers understand and leverage AI tools effectively in their workflows.

## ESI Academy Integration

The `modules.json` file is the primary configuration file that the ESI Academy landing page reads from to display available training modules. This JSON file defines all the course modules, their metadata, and links them to their corresponding content files.

### modules.json Properties

Each module in the `modules.json` file contains the following properties:

- **`id`**: Unique identifier for the module
- **`title`**: Display name of the module shown on the landing page
- **`description`**: Brief summary of what the module covers
- **`icon`**: Icon name used for visual representation
- **`color`**: CSS gradient classes for styling the module card
- **`difficulty`**: Learning level (Beginner, Intermediate, Advanced, Expert)
- **`topics`**: Array of relevant topic tags for categorization
- **`module_path`**: **Critical** - Specifies the location of the actual content markdown file

### Important Note About module_path

The `module_path` property is essential for the ESI Academy landing page functionality. This property tells the program where to find the actual content markdown file for each module. 

- **With module_path**: The landing page will display the full module content when clicked
- **Without module_path**: The landing page will show "Coming Soon" instead of the actual content

Make sure every module that should be accessible has a valid `module_path` pointing to an existing markdown file in the `content/` directory.

## Repository Structure

```
ai-training-content/
├── modules.json              # ESI Academy configuration file
├── README.md                # This documentation file
├── content/                 # Training module content files
│   ├── agentic-ai-course.md
│   ├── copilot-essentials.md
│   ├── cursor-quickstart.md
│   ├── fundamentals.md
│   ├── predictive-vs-generative.md
│   └── prompt-engineering.md
└── promtps/                 # Example prompts and templates
    ├── copilot.md
    └── prompt-engineering.md
```

### Directory Descriptions

- **`modules.json`**: Main configuration file that defines all available training modules for the ESI Academy landing page
- **`content/`**: Contains the actual training material markdown files referenced by `module_path` in `modules.json`
- **`promtps/`**: Collection of example prompts and templates for various AI tools and techniques

## How to Use
1. Navigate to the `content` directory for detailed guides and training modules.
2. Explore the `promtps` directory for example prompts to use with AI tools.
3. Use the resources to enhance your understanding and application of AI in software development.