# Java Text Editor 📝

A feature-rich text editor built with Java Swing that provides essential text editing capabilities with a user-friendly graphical interface.

## 🚀 Features

### Core Text Editing
- **Rich Text Area**: Multi-line text editing with word wrap
- **Scrollable Interface**: Vertical scrolling for large documents
- **Font Customization**: Choose from all available system fonts
- **Font Size Control**: Adjustable font size using spinner control
- **Color Selection**: Change text color with built-in color chooser

### File Operations
- **Open Files**: Load text files (.txt) from your system
- **Save Files**: Save your work to text files
- **File Filtering**: Automatic .txt file filtering in file dialogs

### User Interface
- **Menu Bar**: Easy access to file operations
- **Toolbar**: Quick access to formatting options
- **Responsive Layout**: Automatic layout adjustment
- **Cross-Platform**: Runs on any system with Java support

## 🛠️ Technical Details

### Architecture
- **Framework**: Java Swing GUI
- **Design Pattern**: Event-driven programming
- **File I/O**: Scanner and PrintWriter for file operations
- **Layout**: FlowLayout for component arrangement

### Key Components
- `JTextArea`: Main text editing component
- `JScrollPane`: Scrollable text area container
- `JMenuBar` & `JMenu`: File operations menu
- `JSpinner`: Font size selection
- `JComboBox`: Font family selection
- `JButton`: Color selection trigger
- `JFileChooser`: File open/save dialogs

### Classes
- **TextEditor**: Main class extending JFrame
  - Implements ActionListener for event handling
  - Manages all GUI components and interactions
  - Handles file I/O operations

## 🚀 Getting Started

### Prerequisites
- Java Development Kit (JDK) 8 or higher
- Any Java IDE (IntelliJ IDEA, Eclipse, VS Code) or command line

### Installation & Running

1. **Clone the repository**
   ```bash
   git clone https://github.com/aliammari1/textEditor.git
   cd textEditor
   ```

2. **Compile the project**
   ```bash
   javac src/*.java
   ```

3. **Run the application**
   ```bash
   java -cp src Main
   ```

### Alternative: Using an IDE
1. Import the project into your Java IDE
2. Run the `Main.java` file
3. The text editor window will open

## 🎯 Usage Guide

### Starting the Editor
- Run the application to open the text editor window
- The editor opens with a default Arial font, size 20

### Editing Text
1. **Type directly** in the main text area
2. **Change font**: Select from the font dropdown menu
3. **Adjust size**: Use the spinner to increase/decrease font size
4. **Change color**: Click the "Color" button to open color picker

### File Operations
1. **Opening Files**:
   - Go to File → Open
   - Select a .txt file from your system
   - Content will be loaded into the editor

2. **Saving Files**:
   - Go to File → Save
   - Choose location and filename
   - Your text will be saved as a .txt file

3. **Exiting**:
   - Go to File → Exit
   - Or close the window

## 🔧 Code Structure

```
textEditor/
├── src/
│   ├── Main.java          # Application entry point
│   └── TextEditor.java    # Main editor class
├── .idea/                 # IntelliJ IDEA project files
├── .komment/             # Documentation files
├── textEditor.iml        # IntelliJ module file
├── .gitignore           # Git ignore rules
└── README.md            # This file
```

### Key Methods

**TextEditor Constructor**
- Initializes all GUI components
- Sets up layout and event listeners
- Configures window properties

**actionPerformed(ActionEvent e)**
- Handles all user interactions
- Font/color changes
- File operations (open/save/exit)

## 🎨 Features in Detail

### Font Management
```java
// Font selection from system fonts
String[] fonts = GraphicsEnvironment.getLocalGraphicsEnvironment().getAvailableFontFamilyNames();
fontBox = new JComboBox(fonts);
```

### Color Selection
```java
// Color chooser dialog
JColorChooser colorChooser = new JColorChooser();
Color color = JColorChooser.showDialog(null, "Choose a color", Color.black);
textArea.setForeground(color);
```

### File I/O Operations
- **Reading**: Uses Scanner with FileNotFoundException handling
- **Writing**: Uses PrintWriter with proper resource management
- **File Filtering**: Restricts to .txt files for better UX

## 🔮 Future Enhancements

### Potential Features
- [ ] **Multiple Document Interface**: Tab support for multiple files
- [ ] **Find & Replace**: Text search and replacement functionality
- [ ] **Undo/Redo**: Action history management
- [ ] **Rich Text Formatting**: Bold, italic, underline support
- [ ] **Print Support**: Direct printing capabilities
- [ ] **Recent Files**: Quick access to recently opened files
- [ ] **Auto-save**: Automatic saving functionality
- [ ] **Line Numbers**: Optional line numbering
- [ ] **Word Count**: Document statistics
- [ ] **Themes**: Dark/light mode support

### Technical Improvements
- [ ] **Better Exception Handling**: More robust error management
- [ ] **Configuration File**: Save user preferences
- [ ] **Plugin System**: Extensible architecture
- [ ] **Internationalization**: Multi-language support

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

### Development Guidelines
- Follow Java naming conventions
- Add comments for complex logic
- Test file operations thoroughly
- Ensure cross-platform compatibility

## 📋 Requirements

### System Requirements
- **Operating System**: Windows, macOS, or Linux
- **Java Version**: JDK 8 or higher
- **Memory**: Minimum 512MB RAM
- **Storage**: 50MB free space

### Dependencies
- Java Standard Library (included with JDK)
- Swing GUI Framework (included with JDK)

## 🐛 Known Issues

- Font changes apply to entire document (not selected text)
- No warning when closing unsaved documents
- Limited to .txt files only

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with Java Swing framework
- Inspired by classic text editors like Notepad
- Uses standard Java libraries for cross-platform compatibility

## 📞 Support

For questions, issues, or contributions:
- Create an issue in this repository
- Contact the development team
- Check Java Swing documentation for GUI-related questions

---

**Simple, effective, and educational** - Perfect for learning Java GUI development! ✨