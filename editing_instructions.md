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
        
        <!-- Option C: Music/Bandcamp post -->
        <div class="post-music" onclick="openModal('modalX')">
            <!-- Paste Bandcamp embed code here -->
            <iframe style="border: 0; width: 100%; height: 120px;" 
                    src="https://bandcamp.com/EmbeddedPlayer/album=XXXXX/size=large/bgcol=ffffff/linkcol=0687f5/tracklist=false/artwork=small/" 
                    seamless>
            </iframe>
            <p style="margin-top: 10px;">Click to read more about this track...</p>
        </div>
        
        <!-- Option D: YouTube video post -->
        <div class="post-video" onclick="openModal('modalX')">
            <!-- YouTube embed code here -->
            <iframe width="100%" height="200" 
                    src="https://www.youtube.com/embed/VIDEO_ID" 
                    title="YouTube video player" 
                    frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                    allowfullscreen>
            </iframe>
            <p style="margin-top: 10px;">Click to read more about this video...</p>
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

**YouTube video post example:**
```html
<div class="timeline-post" data-date="2025-08-14">
    <div class="post-date">08.14.2025</div>
    <div class="post-content">
        <div class="post-video" onclick="openModal('modal7')">
            <iframe width="100%" height="200" 
                    src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
                    title="YouTube video player" 
                    frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                    allowfullscreen>
            </iframe>
            <p style="margin-top: 10px;">Behind the scenes of my latest recording session...</p>
        </div>
    </div>
</div>
```

**Music post example:**
```html
<div class="timeline-post" data-date="2025-08-14">
    <div class="post-date">08.14.2025</div>
    <div class="post-content">
        <div class="post-music" onclick="openModal('modal6')">
            <iframe style="border: 0; width: 100%; height: 120px;" 
                    src="https://bandcamp.com/EmbeddedPlayer/album=1234567890/size=large/bgcol=ffffff/linkcol=0687f5/tracklist=false/artwork=small/" 
                    seamless>
            </iframe>
            <p style="margin-top: 10px;">New ambient piece I've been working on...</p>
        </div>
    </div>
</div>
```

**In the modals section:**
```html
<div class="timeline-post" data-date="2025-08-14">
    <div class="post-date">08.14.2025</div>
    <div class="post-content">
        <div class="post-large" onclick="openModal('modal6')"
             style="background-image: url('./images/my-studio-photo.jpg');">
            <div class="post-title">STUDIO SESSION</div>
            <div class="post-avatar">🎤</div>
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
            <h2>Studio Session</h2>
            <div class="full-date">August 14, 2025</div>
            <p>Set up my home studio for the first time today. The acoustics are surprisingly good!</p>
            <img src="./images/my-studio-photo.jpg" alt="My studio setup">
            <p>There's something about having your own creative space that changes everything.</p>
        </div>
    </div>
</div>
```

## 🎨 Customization Options

### Image URLs
You have several options for using your own images:

#### Option 1: GitHub Repository (Recommended)
Upload images directly to your GitHub repo:
1. In your GitHub repository, click "Add file" → "Upload files"
2. Drag and drop your image files (JPG, PNG, etc.)
3. Commit the files
4. Use this URL format: `url('./your-image-name.jpg')`

#### Option 2: Images Folder (Best Organization)
Create an organized folder structure:
1. In your repo, click "Create new file"
2. Type: `images/placeholder.txt` (this creates the folder)
3. Commit this file
4. Upload your images to the `images/` folder
5. Use this URL format: `url('./images/your-photo.jpg')`

#### Option 3: External Hosting
Use free image hosting services:
- **Imgur.com** - Upload image, get direct link
- **Google Photos** - Share image, get link
- **GitHub Issues trick** - Create new issue, drag image into text box, copy generated URL

#### Option 4: Unsplash (Free Stock Images)
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

## 🎵 Adding Music Posts (Bandcamp)

### Getting Bandcamp Embed Code
1. Go to the album/song page on Bandcamp
2. Click "Share/Embed" (usually under the player)
3. Copy the embed code (iframe tag)
4. Choose your preferred player size

### Music Post Template
```html
<div class="timeline-post" data-date="YYYY-MM-DD">
    <div class="post-date">MM.DD.YYYY</div>
    <div class="post-content">
        <div class="post-music" onclick="openModal('modalX')">
            <!-- Paste your Bandcamp embed code here -->
            <iframe style="border: 0; width: 100%; height: 120px;" 
                    src="YOUR_BANDCAMP_EMBED_URL" 
                    seamless>
            </iframe>
            <p style="margin-top: 10px;">Click to read more about this track...</p>
        </div>
    </div>
</div>
```

### Required CSS Addition
Add this CSS to your `index.html` in the `<style>` section:
```css
.post-music {
    line-height: 1.6;
    cursor: pointer;
    padding: 10px;
}

.post-music iframe {
    border-radius: 4px;
    margin-bottom: 10px;
}

.post-music:hover {
    background-color: rgba(0,0,0,0.02);
}

.post-video {
    line-height: 1.6;
    cursor: pointer;
    padding: 10px;
}

.post-video iframe {
    border-radius: 4px;
    margin-bottom: 10px;
}

.post-video:hover {
    background-color: rgba(0,0,0,0.02);
}
```

### Music Post Examples
- **Your own releases:** Share your latest tracks or albums
- **Favorite discoveries:** Highlight music that inspires you
- **Collaborations:** Feature work with other artists
- **Work in progress:** Share demos or rough mixes

### YouTube Video Examples
- **Behind the scenes:** Recording sessions, studio tours
- **Performances:** Live shows, acoustic sessions
- **Tutorials:** How you create certain sounds or techniques
- **Inspiration:** Videos that influence your work
- **Collaborations:** Video projects with other artists

## 📷 Working with Images

### Image Requirements
- **Formats:** JPG, PNG, GIF, WebP
- **Size:** Recommend 800px wide or larger for best quality
- **File size:** Keep under 5MB for fast loading
- **Aspect ratio:** Horizontal/landscape images work best for large posts

### Adding Images to Modal Content
You can also add images inside the modal content:
```html
<div class="full-post">
    <h2>Your Post Title</h2>
    <div class="full-date">Month Day, Year</div>
    <p>Your text content here...</p>
    <img src="./images/your-photo.jpg" alt="Description of image">
    <p>More text after the image...</p>
</div>
```

### Organizing Your Images
**Recommended folder structure:**
```
yourusername.github.io/
├── index.html
├── EDITING_INSTRUCTIONS.md
├── images/
│   ├── studio-photo.jpg
│   ├── forest-walk.jpg
│   └── equipment-setup.png
└── README.md
```

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
