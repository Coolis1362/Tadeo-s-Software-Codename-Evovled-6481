# **TS-GUI NT**  

**Codename: Evolved**
**Build: 6481**

TS-GUI NT is a graphical user interface built using Python and Pygame, designed by **Tadeo's Software**. It acts as the GUI component for the TS-DOS system, offering a retro-modern aesthetic and interactive functionality that complements command-line operations.

## **Features**  

- **About Window**: Displays detailed version information, including the current build and language pack.  
- **Interactive Buttons**: Three functional buttons:  
  - **Internet**: Opens a web browser (Google).  
  - **Email**: Launches Outlook.  
  - **TS-GUI Version**: Displays a custom "About" window with version details.  
- **Customizable GUI**: Includes hover effects, color customization, and modular design.  
- **Start Button**: A dedicated button for quick access to additional functions or apps.

## **Setup and Installation**

### **Requirements**  

- Python **3.13 or later**  
- Pygame library

### **Installation Steps**  

1. Install Python:  
   - Download and install Python from [python.org](https://www.python.org/).  
   - Ensure Python is added to the system PATH.  

2. Install Pygame:  
   - Open a terminal/command prompt and run:  

     ```bash
     pip install pygame
     ```  

3. Clone or download this repository.  

4. Run the TS-GUI NT script:  

   ```bash
   cd C:\Users\usernamehere\Path\To\Your\LOCALTSEVOVLED REM Replace C:\Users\usernamehere\Path\To\Your\LOCALTSEVOVLED With The Actal Path to your LOCALTSEVOVLED
   ts-guint REM When ts-guint Is Typed It Should start Evovled Build 6481
   ```

## **Usage**

1. **Launch TS-GUI**:  
   - Start the program, and the main screen will load with several interactive buttons.  

2. **Explore Functionality**:  
   - **Internet**: Click to open Google in the default web browser.  
   - **Email**: Click to launch Microsoft Outlook (requires Outlook to be installed).  
   - **TS-GUI Version**: Displays version details, language pack info, and codename.  

3. **Exit**:  
   - Close the application using the `X` button in the top-right corner of the window.

## **Code Overview**

### **1. About Window**

The `show_version_info` function creates a pop-up window displaying detailed information about the current TS-GUI version.

```python
def show_version_info():
    # Create a new "About" surface
    about_width, about_height = 400, 200
    about_screen = pygame.Surface((about_width, about_height))
    about_screen.fill((255, 255, 255))  # Set white background

    # Add text for the version and language pack
    font = pygame.font.Font(None, 36)
    title = font.render("About TS-GUI NT", True, (0, 0, 0))  # Black text
    version = font.render("TS-GUI: EVOLVED", True, (0, 0, 0))
    about_screen.blit(title, (50, 50))
    about_screen.blit(version, (50, 100))
    ...
