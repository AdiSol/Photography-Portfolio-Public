# Picture Content Management Instructions

## Overview
Your photography portfolio is organized into two main categories:
- **Horizontal**: Landscape-oriented photos (16:10 or similar aspect ratios)
- **Vertical**: Portrait-oriented photos (3:4 or similar aspect ratios)

Each picture shows a **before and after comparison** with an interactive slider that visitors can drag to see the difference between the raw and edited versions.

## File to Edit
**Main file**: `public/content/pictures/pictures.json`

This single file controls all pictures displayed on your website.

## Required Folder Structure

For each picture, you need to create a folder structure like this:

```
public/content/pictures/
├── pictures.json                    # Main configuration file
├── horizontal/                      # Landscape photos
│   ├──project-name-1 raw.jpg                  # Before image
│   └──project-name-1 edit.jpg               # After image
│   ├── project-name-2 raw.jpg
│   └──project-name-2 edit.jpg
│   └── ...
├── vertical/                        # Portrait photos
│   ├── project-name-1 raw.jpg                  # Before image
│   └──project-name-1 edited.jpg               # After image
│   ├── project-name-2 raw.jpg
│   └──project-name-2 edit.jpg
│   └── ...
└── README-CLIENT-INSTRUCTIONS.md    # This file
```

## Picture Properties Explained

Each picture has these required properties:

```json
{
  "id": "unique-picture-name",           // Must match folder name
  "title": "Picture Title",              // Displayed under the comparison
  "description": "Editing description",  // What editing was done
  "category": "horizontal",              // Must match category id
  "rawImage": "/content/pictures/horizontal/picture-name/raw.jpg",
  "editedImage": "/content/pictures/horizontal/picture-name/edited.jpg",
  "orientation": "horizontal"            // "horizontal" or "vertical"
}
```

## Adding a New Picture

### Step 2: Create Folder Structure
1. **Choose the right category**:
   - `horizontal` for landscape photos (wider than tall)
   - `vertical` for portrait photos (taller than wide)

2. **Create a project folder**:
   - Use lowercase letters and hyphens only
   - Example: `sunset-landscape-edit` or `portrait-headshot-session`

3. **Upload your images**:
   ```
   public/content/pictures/horizontal
   ├──sunset-landscape raw.jpg    # Original photo
   └──sunset-landscape edit.jpg # Your edited version
   ```

### Step 3: Update the JSON File
Add your picture to the appropriate category in `pictures.json`:

```json
{
  "id": "sunset-landscape-edit",
  "title": "Golden Hour Landscape Enhancement",
  "description": "Enhanced colors, improved contrast, and sky replacement to create a dramatic sunset scene with warmer tones and better exposure balance.",
  "category": "horizontal",
  "rawImage": "/content/pictures/horizontal/sunset-landscape raw.jpg",
  "editedImage": "/content/pictures/horizontal/sunset-landscape edit.jpg",
  "orientation": "horizontal"
}
```

## Picture Ordering

Pictures appear in the carousel in the **exact order** they're listed in the JSON file:
- **First picture** = Default picture for that category
- **Reorder** by cutting and pasting entire picture objects
- **Best work** should be placed first in each category
- **No JSON File Option** Optionally you can just delete the json file and the ordering will be based on the alphabetically ordering of the filenames and the picture title will be taken from the filename

## Category Guidelines

### Horizontal Pictures
- **Landscape orientation** (wider than tall)
- **Examples**: Landscapes, architecture, automotive, group photos
- **Best aspect ratios**: 16:10, 3:2, 16:9
- **Display**: Wide comparison slider

### Vertical Pictures
- **Portrait orientation** (taller than wide)
- **Examples**: Portraits, fashion, street photography, product shots
- **Best aspect ratios**: 3:4, 2:3, 4:5
- **Display**: Tall comparison slider, centered layout

## Image Requirements

### File Naming
- **Always use**: `raw.jpg` and `edit.jpg` at the end of your filenames
- **Folder names**: Use descriptive names with hyphens
- **Avoid**: Spaces, special characters, uppercase letters

### Image Quality
- **Resolution**: 
  - Horizontal: 1920px wide maximum
  - Vertical: 1920px tall maximum
- **File size**: Under 1MB per image for fast loading
- **Format**: JPG for photographs
- **Quality**: 80-85% compression for good balance

### Before/After Guidelines
- **Raw image**: Should show the unedited state clearly
- **Edited image**: Your final edit showcasing your skills
- **Same composition**: Both images should have identical framing
- **Highlight improvements**: Choose edits that clearly show your expertise

## Example: Complete Picture Entry

```json
{
  "id": "car-commercial-retouch",
  "title": "Automotive Commercial Photography",
  "description": "Professional car photography with studio lighting simulation, background replacement, paint enhancement, and detail sharpening. Transformed a parking lot shoot into a showroom-quality image.",
  "category": "horizontal",
  "rawImage": "/content/pictures/horizontal/car-commercial-retouch raw.jpg",
  "editedImage": "/content/pictures/horizontal/car-commercial-retouch edit.jpg",
  "orientation": "horizontal"
}
```

## Best Practices

### For Picture Titles:
- Keep under 50 characters
- Be descriptive and professional
- Include the type of photography or subject
- Example: "Wedding Portrait Enhancement" not "Photo 1"

### For Descriptions:
**Optional: But currently is not reflected on the website**
- Explain what editing techniques you used
- Mention specific improvements (color, lighting, retouching)
- Keep it informative but not too technical
- Show your expertise and attention to detail

### For File Organization:
- Use consistent folder naming
- Keep raw and edited versions in sync
- Back up your original files separately
- Test images before uploading

## Image Protection Features

Your images include several protection measures:
- **Right-click disabled** on comparison area
- **Drag and drop disabled** 
- **User selection disabled**
- **Download prevention** (basic level)

**Note**: These provide basic protection but determined users can still capture images. Focus on showcasing your work while maintaining some protection.

## Removing Pictures

To remove a picture:
1. **Delete the folder** from the file system
2. **Remove the entry** from the JSON file
3. **Check for trailing commas** in the JSON

## Common Mistakes to Avoid

❌ **Don't do this:**
- Use spaces in folder names (`"my photo"`)
- Forget to upload both raw.jpg and edited.jpg
- Use different compositions for before/after
- Make file sizes too large (over 1MB each)
- Mix up orientation values

✅ **Do this:**
- Use hyphens in folder names (`"my-photo"`)
- Always include both versions
- Keep identical framing between versions
- Optimize images for web
- Match orientation to actual image orientation

## Testing Your Changes

After making changes:
1. **Validate JSON syntax** using an online JSON validator
2. **Check file paths** match exactly what's in your folders
3. **Test image loading** on your website
4. **Try the slider** to ensure smooth operation
5. **Test on mobile** devices for responsive behavior

## Troubleshooting

### Images Not Loading:
- Check file paths in JSON match actual folder structure
- Ensure file names are exactly `raw.jpg` and `edit.jpg`
- Verify images are in the correct category folder

### Slider Not Working:
- Make sure both raw and edited images exist
- Check that image dimensions are reasonable
- Verify images are web-optimized

### Layout Issues:
- Confirm orientation value matches actual image orientation
- Check that images are properly cropped/sized
- Test on different screen sizes

## Getting Help

If you encounter issues:
1. **JSON Syntax**: Use [JSONLint](https://jsonlint.com/) to validate
2. **File Paths**: Double-check folder and file names
3. **Image Issues**: Verify image quality and size
4. **Still Having Problems**: Contact your developer with specific error messages

---

## Quick Reference: Folder Structure

```
public/content/pictures/
├── pictures.json
├── horizontal/
│   ├──project-1 raw.jpg
│   └──project-1 edited.jpg
│   ├──project-2 raw.jpg
│    └──project-2 edited.jpg
├── vertical/
│   ├── portrait-1 raw.jpg
│   └──portrait-1 edited.jpg
│   ├──portrait-2 raw.jpg
│   └──portrait-2 edited.jpg
└── README-CLIENT-INSTRUCTIONS.md
```

## Quick Reference: JSON Structure

```json
{
  "title": "Picture",
  "description": "See the difference!",
  "categories": [
    {
      "id": "horizontal",
      "name": "Horizontal",
      "pictures": [
        {
          "id": "folder-name",
          "title": "Picture Title",
          "description": "What editing was done",
          "category": "horizontal",
          "rawImage": "/content/pictures/horizontal/folder-name raw.jpg",
          "editedImage": "/content/pictures/horizontal/folder-name edit.jpg",
          "orientation": "horizontal"
        }
      ]
    }
  ]
}
```

---

**Remember**: The first picture in each category will be displayed by default. Arrange your pictures with your best work first to make a strong first impression!1: Prepare Your Images
1. **Export two versions** of your photo:
   - `raw.jpg` - The original, unedited version
   - `edit.jpg` - Your final edited version
2. **Optimize for web**:
   - Horizontal photos: Max width 1920px
   - Vertical photos: Max height 1920px
   - Keep file sizes under 1MB each for fast loading
   - Use JPG format for photos