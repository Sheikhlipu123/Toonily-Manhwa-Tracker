# Toonily Manhwa Tracker

A comprehensive Tampermonkey userscript that automatically tracks your manhwa reading progress on Toonily.com. Keep track of what you've read, when you read it, and never lose your place again!

## Features

### 🔄 Automatic Tracking
- Automatically detects and tracks manhwa from Toonily URLs
- Extracts manhwa names and chapter information seamlessly
- No manual input required - just browse normally

### 📊 Reading Progress
- Tracks which chapters you've read and when
- Records reading frequency and timestamps
- Shows total chapters read per manhwa
- Maintains complete reading history

### 🖼️ Visual Collection
- Automatically captures manhwa cover thumbnails
- Clean, organized display of your collection
- Visual progress indicators

### 💾 Persistent Storage
- Uses browser localStorage for permanent data storage
- Data persists across browser sessions
- No external servers or accounts required

### 🔍 Search & Filter
- Search through your tracked manhwa collection
- Filter by reading status or progress
- Quick access to specific titles

### 📱 User-Friendly Interface
- Floating tracker button for easy access
- Comprehensive popup interface
- Responsive design that works on all screen sizes
- Clean, modern UI

### 💼 Data Management
- Export your tracking data for backup
- Import data from other devices
- Clear individual manhwa or entire collection

## Installation

### Prerequisites
- [Tampermonkey](https://www.tampermonkey.net/) browser extension
- Access to Toonily.com

### Steps
1. **Install Tampermonkey**
   - Chrome: [Chrome Web Store](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
   - Firefox: [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)
   - Edge: [Microsoft Store](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd)

2. **Install the Script**
   - Copy the script from `toonily-manhwa-tracker.user.js`
   - Open Tampermonkey dashboard
   - Click "Create a new script"
   - Paste the code and save (Ctrl+S)

3. **Enable the Script**
   - Ensure the script is enabled in Tampermonkey
   - Visit any Toonily manhwa page to start tracking

## Usage

### Basic Usage
1. **Automatic Tracking**: Simply visit any manhwa page on Toonily.com
   - The script automatically detects and tracks the manhwa
   - Chapter progress is recorded when you visit chapter pages

2. **View Collection**: Click the "📚 Tracker" button (top-right corner)
   - See all your tracked manhwa
   - View reading progress and statistics
   - Access detailed chapter history

### Interface Guide

#### Main Panel
- **Search Bar**: Find specific manhwa in your collection
- **Manhwa Cards**: Visual display with thumbnails and progress
- **Chapter Count**: Shows chapters read vs total available
- **Last Read**: Displays when you last read each manhwa

#### Chapter Details
- Click on any manhwa card to see detailed chapter history
- View reading dates and frequency
- See complete chapter progression

#### Data Management
- **Export**: Download your tracking data as JSON
- **Import**: Upload previously exported data
- **Clear**: Remove individual manhwa or entire collection

## URL Pattern Recognition

The script automatically recognizes these URL patterns:

### Manhwa Pages
\`\`\`
https://toonily.com/serie/[manhwa-name]/
\`\`\`
Example: `https://toonily.com/eleceed/my/`

### Chapter Pages
\`\`\`
https://toonily.com/serie/[manhwa-name]/chapter-[number]/
\`\`\`
Example: `https://toonily.com/serie/eleceed/chapter-1/`

## Data Structure

The script stores data in the following format:
\`\`\`javascript
{
  "manhwa-name": {
    "name": "Display Name",
    "thumbnail": "image-url",
    "chapters": {
      "1": {
        "readCount": 1,
        "firstRead": "2024-01-01T12:00:00.000Z",
        "lastRead": "2024-01-01T12:00:00.000Z"
      }
    },
    "totalChapters": 10,
    "lastVisited": "2024-01-01T12:00:00.000Z"
  }
}
\`\`\`

## Browser Compatibility

- ✅ Chrome (Recommended)
- ✅ Firefox
- ✅ Edge
- ✅ Safari (with Tampermonkey)
- ✅ Opera

## Privacy & Security

- **Local Storage Only**: All data is stored locally in your browser
- **No External Requests**: Script doesn't send data to external servers
- **No Personal Information**: Only tracks reading progress, no personal data
- **Open Source**: Full code is available for review

## Troubleshooting

### Script Not Working
1. Ensure Tampermonkey is installed and enabled
2. Check if the script is enabled in Tampermonkey dashboard
3. Refresh the Toonily page
4. Check browser console for errors

### Data Not Saving
1. Ensure localStorage is enabled in your browser
2. Check if you're in incognito/private mode (data won't persist)
3. Verify sufficient storage space

### Tracker Button Not Visible
1. Check if the script is running on the correct domain
2. Disable other extensions that might interfere
3. Try refreshing the page

## Contributing

Contributions are welcome! Please feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

[**sheikhlipu123**](https://github.com/Sheikhlipu123)

## Changelog

### v1.0.0
- Initial release
- Automatic manhwa and chapter tracking
- Persistent localStorage storage
- Visual collection interface
- Search and filter functionality
- Export/import capabilities
- Thumbnail extraction

## Support

If you encounter any issues or have questions:
1. Check the troubleshooting section above
2. Open an issue on GitHub
3. Provide browser version and error details for faster resolution

---

**Enjoy tracking your manhwa reading progress!**
