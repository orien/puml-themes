# PlantUML Themes

A collection of beautiful, professionally designed themes for PlantUML diagrams. Create stunning documentation with consistent styling and color palettes that enhance readability and visual appeal.

## 🎨 Available Themes

### Solarized Light
A carefully crafted light theme based on Ethan Schoonover's acclaimed [Solarized color palette](https://ethanschoonover.com/solarized/). This theme provides excellent readability and a professional appearance for all your PlantUML diagrams.

**Features:**
- Optimized color contrast for better readability
- Professional appearance suitable for documentation
- Based on the popular Solarized color scheme

## 📦 Installation & Usage

### Quick Start

1. **Download the theme file:**
   ```bash
   wget https://raw.githubusercontent.com/yourusername/puml-themes/main/themes/puml-theme-solarized-light.puml
   ```

2. **Include in your PlantUML diagram:**
   ```plantuml
   @startuml
   !include puml-theme-solarized-light.puml

   Alice -> Bob: Hello
   Bob --> Alice: Hi!
   @enduml
   ```

### Local Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/puml-themes.git
   ```

2. Reference the theme in your diagrams:
   ```plantuml
   @startuml
   !include ./puml-themes/themes/puml-theme-solarized-light.puml

   participant User
   participant System
   participant Database

   User -> System: Request data
   System -> Database: Query
   Database --> System: Results
   System --> User: Response
   @enduml
   ```

### Remote Include (Recommended)

For the latest version, include directly from the repository:

```plantuml
@startuml
!include https://raw.githubusercontent.com/yourusername/puml-themes/main/themes/puml-theme-solarized-light.puml

' Your diagram content here
@enduml
```

## 🖼️ Gallery

### Sequence Diagrams

The Solarized Light theme provides beautiful styling for sequence diagrams with clear participant boxes, readable fonts, and subtle color accents.

![Sequence Participants](themes/puml-theme-solarized-light.md#gallery)

*See the full gallery in [themes/puml-theme-solarized-light.md](themes/puml-theme-solarized-light.md)*

## ⚙️ Customization

### Font Configuration

You can customize the font family and size by setting variables before including the theme:

```plantuml
@startuml
!$FONT_NAME = "Arial"
!$FONT_SIZE = 14
!include puml-theme-solarized-light.puml

' Your diagram here
@enduml
```

### Available Variables

- `$FONT_NAME` - Font family (default: "Verdana")
- `$FONT_SIZE` - Base font size (default: 12)
- `$TITLE_SIZE` - Title font size (automatically calculated as $FONT_SIZE + 4)

## 🛠️ Development Tools

This repository includes powerful tools for theme development and gallery generation:

### Gallery Generation
- **Location:** `tools/gallery-generation/`
- **Purpose:** Automatically generate visual galleries of themes applied to different diagram types
- **Usage:** Creates comparison images for documentation and testing

### Input Templates
- **Location:** `tools/input/`
- **Purpose:** Sample diagrams for testing themes across different PlantUML diagram types
- **Includes:** Activity, Class, Sequence, State, Use Case, and many more diagram examples



## 📚 Resources

- [PlantUML Official Documentation](https://plantuml.com/)
- [PlantUML Skinparam Reference](https://plantuml.com/skinparam)
- [Solarized Color Palette](https://ethanschoonover.com/solarized/)
- [PlantUML Themes Gallery](https://the-lum.github.io/puml-themes-gallery/)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Acknowledgments

- [Ethan Schoonover](https://ethanschoonover.com/) for the original Solarized color palette
- The PlantUML community for creating an amazing diagramming tool
- Contributors who have helped improve and expand this theme collection

---

**Made with ❤️ for the PlantUML community**
