# Timeline Blog - Editing Instructions

This file contains instructions for adding and editing posts on your timeline blog. This file won't appear on your website - only in your GitHub repository.

## 📝 How to Add New Posts

### Step 1: Add the Post HTML
In your `index.html` file, find the `<div class="timeline">` section and add a new post using this template:

```html
<div class="timeline-post" data-date="YYYY-MM-DD">
    <div class="post-date">MM.DD.YYYY</div>
    <div class="post-content">
        <!-- Choose ONE of these two options: -->
        
        <!-- Option A: Text-only post -->
        <div class="post-text" onclick="openModal('modalX')">
            <p>Your preview text here...</p>
        </div>
        
        <!-- Option B: Large image post -->
        <div class="post-large" onclick="openModal('modalX')"
             style="background-image: url('YOUR_IMAGE_URL');">
            <div class="post-title">YOUR TITLE</div>
            <div class="post-avatar">🎵</div>
        </div>
    </div>
</div>
```

### Step 2: Add the Modal
In the modals section (after `<!-- Modals -->`), add:

```html
<div id="modalX" class="modal">
    <div class="modal-content">
        <button class="close" onclick="closeModal('modalX')">&times;</button>
        <div class="full-post">
            <h2>Your Post Title</h2>
            <div class="full-date">Month Day, Year</div>
            <p>Your full blog post content goes here.</p>
            <p>You can add multiple paragraphs.</p>
        </div>
    </div>
</div>
```

## 🛠️ Complete Example

Let's add a post for August 14, 2025:

**In the timeline section:**
```html
<div class="timeline-post" data-date="2025-08-14">
    <div class="post-date">08.14.2025</div>
    <div class="post-content">
        <div class="post-text" onclick="openModal('modal6')">
            <p>Experimenting with new recording techniques...</p>
        </div>
    </div>
</div>
```

**In the modals section:**
```html
<div id="modal6" class="modal">
    <div class="modal-content">
        <button class="close" onclick="closeModal('modal6')">&times;</button>
        <div class="full-post">
            <h2>New Recording Techniques</h2>
            <div class="full-date">August 14, 2025</div>
            <p>Today I tried a completely different approach to capturing ambient sounds. The results were surprisingly different from my usual methods.</p>
            <p>There's something about changing your technique that opens up new creative possibilities.</p>
        </div>
    </div>
</div>
```

## 🎨 Customization Options

### Image URLs
Use free images from Unsplash:
- `https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=800`
- `https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=800`
- `https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?w=800`

### Avatar Emojis
- 🎵 Music/Sound
- 🌲 Nature/Forest  
- ☀️ Summer/Sun
- 🏙️ Urban/City
- 🌙 Night/Evening
- 🎤 Recording
- 📻 Radio/Audio
- 🔊 Speakers/Sound

### Date Format
- **data-date:** Always use `"YYYY-MM-DD"` format (e.g., "2025-08-14")
- **Display date:** Use `MM.DD.YYYY` format (e.g., "08.14.2025")
- **Modal date:** Use `Month Day, Year` format (e.g., "August 14, 2025")

## ⚠️ Important Rules

1. **Unique Modal IDs:** Each post needs a unique modal ID (modal6, modal7, modal8, etc.)
2. **Date Format:** Must use `data-date="YYYY-MM-DD"` for time-scaling to work correctly
3. **Post Order:** Doesn't matter where you add posts - JavaScript sorts by date automatically
4. **Time Spacing:** Posts are spaced 5px per day apart on the timeline

## 🔧 Time Spacing

The timeline automatically spaces posts based on real time:
- Posts from the same day: Very close together (may overlap on alternating sides)
- Posts 1 week apart: 35px spacing
- Posts 1 month apart: ~150px spacing

## 📂 File Structure

Your repository should have:
- `index.html` - Your main website file
- `EDITING_INSTRUCTIONS.md` - This file (won't show on website)
- `README.md` - Optional description file

## 🚀 Publishing Changes

1. Edit `index.html` on GitHub
2. Add your new post HTML and modal
3. Commit changes
4. Your website updates automatically!

## 💡 Tips

- **Test locally:** You can download the HTML file and open it in your browser to test changes
- **Backup:** GitHub automatically keeps version history of all your changes
- **Preview:** Use the GitHub file preview to check your markdown formatting
- **Inspiration:** Look at existing posts in the code to see the pattern

Happy blogging! 🎉