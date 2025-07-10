# Quiz Academy - Multipurpose Quiz Application

A static web application for creating and taking quizzes across multiple courses and modules. Perfect for certification exam preparation, training programs, and educational content.

## Features

- 📚 **Multi-Course Support** - Organize quizzes by courses and modules
- 🎯 **Flexible Module Selection** - Choose specific modules or all modules from a course
- 📱 **Responsive Design** - Works on desktop, tablet, and mobile devices
- 🔀 **Question Shuffling** - Randomizes question order for each quiz attempt
- 📊 **Real-time Statistics** - Track progress and performance
- 🎨 **Modern UI** - Clean, professional interface with smooth animations
- 🚀 **GitHub Pages Ready** - Deploy easily as a static site

## Quick Start

1. **Clone or download** this repository
2. **Create your question files** in YAML format (see examples below)
3. **Configure** your courses in `quizes.yml`
4. **Deploy** to GitHub Pages or any static hosting service

## File Structure

```
quiz-academy/
├── index.html              # Main application file
├── quizes.yml              # Course and module configuration
├── for509/                 # FOR509 question files
│   ├── for509_day1_questions.yml
│   ├── for509_day2_questions.yml
│   └── ...
├── custom/                 # Custom topic question files
│   ├── python_security_questions.yml
│   └── ...
└── README.md              # This file
```

## Configuration

### 1. Main Configuration (`quizes.yml`)

Configure your courses and modules in the `quizes.yml` file:

```yaml
courses:
  "Course Name":
    description: "Course description"
    modules:
      "Module 1 Name": "path/to/module1_questions.yml"
      "Module 2 Name": "path/to/module2_questions.yml"
```

### 2. Question Files

Each module should have its own YAML file with questions:

```yaml
metadata:
  title: "Module Title"
  created_by: "Your Name"
  content_source: "Source Material"
  question_count: 30

questions:
  - category: "Category Name"
    type: "multiple_choice"
    question: "Your question here?"
    options:
      - "Option A"
      - "Option B"
      - "Option C"
      - "Option D"
    correct_answer: "Option B"
    explanation: "Explanation of why this answer is correct."

  - category: "Category Name"
    type: "true_false"
    question: "True or false statement?"
    correct_answer: true
    explanation: "Explanation of the answer."
```

### Question Types Supported

1. **Multiple Choice** (`multiple_choice`)
   - 4 answer options
   - Single correct answer
   
2. **True/False** (`true_false`)
   - Boolean questions
   - Answer: `true` or `false`

3. **Fill in the Blank** (`fill_blank`) (not tested)
   - Text input questions
   - Case-insensitive matching

Your quiz will be available at: `https://quiz.dropfra.me/`

## Creating Question Files

### Using the Question Generation Prompt

You can use the included question generation prompt with AI assistants to create questions:

1. Provide your training material
2. Use the prompt from the original documents
3. Generate questions in the required YAML format
4. Save to appropriate module files

### Manual Question Creation

Follow the YAML format shown in the examples. Key points:

- **Categories**: Group related questions
- **Explanations**: Always include detailed explanations
- **Variety**: Mix question types and difficulty levels
- **Accuracy**: Ensure all answers are correct and explanations are clear

## Customization

### Styling

Modify the CSS in `index.html` to match your brand:

- Colors: Update the CSS variables at the top of the style section
- Fonts: Change the `font-family` property
- Layout: Adjust grid layouts and spacing

### Features

The application is modular and easy to extend:

- Add new question types by modifying the `renderQuestionOptions()` method
- Implement time limits by adding timer functionality
- Add question categories filtering
- Implement progress saving using localStorage

## Dependencies

- **js-yaml**: For parsing YAML files (loaded from CDN)
- **Modern browser**: Supports ES6+ features

## Example Use Cases

- **Certification Exam Prep**: SANS, Cisco, CompTIA, etc.
- **Self-Study**: Personal knowledge testing

## Contributing

1. Fork the repository
2. Create your feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

---

**Happy Learning! 🎓**
