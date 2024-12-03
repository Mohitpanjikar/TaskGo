# TaskGo

Welcome to **TaskGo**, a simple and efficient CLI Todo application built with Go! This project demonstrates how to create a command-line interface for managing todos while showcasing Go's functionality for handling JSON data and command-line arguments.

---

![Add Todo Screenshot](https://github.com/Mohitpanjikar/TaskGo/blob/main/buildcli.png)
![Add Todo Screenshot](https://github.com/Mohitpanjikar/TaskGo/blob/main/CLI.png)

## Features

- **Add Todos**: Easily create new tasks with titles.
- **Delete Todos**: Remove tasks by specifying their index.
- **Toggle Completion**: Mark tasks as completed or incomplete.
- **Edit Todos**: Modify the title of an existing task.
- **List Todos**: View all tasks in a structured table format.
- **Persistent Storage**: Save and load todos to/from a JSON file.
- **Command-Line Arguments**: Perform all operations via intuitive CLI commands.

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/TaskGo.git
   cd TaskGo
   ```

2. **Install dependencies**:
   Ensure you have Go installed. Then, fetch any required packages:
   ```bash
   go mod tidy
   ```

3. **Build the project**:
   ```bash
   go build -o taskgo main.go
   ```

4. **Run the application**:
   ```bash
   ./taskgo
   ```

---

## Usage

### Commands Overview

- **Add a Todo**:
  ```bash
  ./taskgo -add="Buy Milk"
  ```

- **List Todos**:
  ```bash
  ./taskgo -list
  ```

- **Delete a Todo**:
  ```bash
  ./taskgo -del=0
  ```

- **Toggle Completion**:
  ```bash
  ./taskgo -toggle=0
  ```

- **Edit a Todo**:
  ```bash
  ./taskgo -edit="0:New Title"
  ```

---

## Project Structure

```
TaskGo/
├── main.go           # Entry point and main logic.
├── todo.go           # Todo structure and related methods.
├── storage.go        # Persistent JSON storage implementation.
├── command.go        # Command-line flag handling.
├── go.mod            # Module file.
└── todos.json        # Sample data file.
```

---


## Key Concepts

- **Todos Management**: All todos are stored in a slice of structs with fields like `Title`, `Completed`, and timestamps for creation and completion.
- **JSON Storage**: Utilizes Go's encoding/json package for saving and loading todos in a readable format.
- **CLI Flags**: Built with the `flag` package, enabling simple yet powerful command-line operations.
- **Tabular Display**: Employs the [aquasecurity/table](https://github.com/aquasecurity/table) package for a clean, formatted output.

---

## Future Enhancements

- Add search functionality for tasks.
- Include deadlines and prioritization.
- Introduce task categorization.
- Add unit tests for robust testing.

---

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for new features or improvements.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments

Special thanks to [Coding with Patrik](https://codingwithpatrik.dev/posts/how-to-build-a-cli-todo-app-in-go/) for the tutorial inspiration.

---

Get started with **TaskGo** and manage your tasks seamlessly via the terminal! 🎉
