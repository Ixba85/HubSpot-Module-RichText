# HubSpot-Module-RichText
# **Paper Container Module**

## **Overview**
The **Paper Container Module** is a flexible content container that allows users to display a title and rich text content. With responsive styling and easy configuration through JSON fields, this module is perfect for creating structured content sections.

---

## **Features**
1. **Content Display:**
   - Supports a customizable title (`title`) and rich text content (`content`).
   - Dynamically renders rich text using HubSpot's `{{ module.content }}`.

2. **Responsive Design:**
   - Adjusts seamlessly for different screen sizes using CSS media queries.
   - Enhanced layout for larger screens with increased width and padding.

3. **Custom Styling:**
   - Clean and modern typography with customizable headings, paragraphs, and links.
   - Hover effects for links enhance the user experience.

---

## **Code Structure**
### **1. HTML**
Defines the structure of the module:
- `div.paper-container`: Main container for the title and content.
- `h1`: Module title.
- `div.paper-content`: Container for rich text content.

### **2. CSS**
Handles the styling:
- **Container Styling:**
  - Centered layout with a max width of `800px` (expanded to `1000px` on larger screens).
  - Borders, padding, and box shadows for a clean look.
- **Typography:**
  - Readable font sizes and line heights for headings (`h2`, `h3`, `h4`) and paragraphs.
  - Custom styles for links with hover effects.
- **Responsive Behavior:**
  - Media query for screens wider than `1200px` to enhance layout and spacing.

### **3. Fields (fields.json)**
Defines the field configurations:
- **`richtext_field`**: A rich text field for adding formatted content such as headings, paragraphs, and links.

### **4. Module Fields (module.js)**
Defines editable fields in the HubSpot editor:
- **`title`**: A text field for the title.
- **`content`**: A rich text field for detailed content.

```json
{
  "fields": [
    {
      "name": "title",
      "label": "Title",
      "type": "text"
    },
    {
      "name": "content",
      "label": "Content",
      "type": "richtext"
    }
  ]
}

