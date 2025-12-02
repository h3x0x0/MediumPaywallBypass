# Medium Bypass

**Description**: A simple bookmarklet that redirects Medium articles behind a paywall to a freemium mirror site.

## How to Create the Bookmark Snippet

1. **Copy the Bookmarklet Code**:  
   Here’s the code you need to create the bookmark:

   ```javascript
   javascript:(function(){if(!location.href.endsWith('#bypass')&&!location.href.includes("/edit?source=")&&document.head.querySelector('meta[property="al:android:url"]').content.includes('medium://p/')){location.href='https://freedium-mirror.cfd/'+location.href;}else if(/(?:.*\.)?medium\.com$/.test(location.host)){new MutationObserver(m=>{if(m[0].target.textContent)mediumRedirecter();}).observe(document.querySelector('title'),{subtree:true,characterData:true,childList:true});}})();

2. **Create a New Bookmark**:  
   - Open your browser's bookmarks manager or press `Ctrl+D` (Windows) / `Command+D` (Mac) to create a new bookmark.

3. **Paste the Code**:  
   - In the "URL" or "Location" field, paste the copied JavaScript code.

4. **Name Your Bookmark**:  
   - Give your bookmark a memorable name, such as **Medium Bypass**.

5. **Save the Bookmark**:  
   - Click "Save" to store your bookmark.

## Usage

- Navigate to any Medium article.
- Click on the **Medium Bypass** bookmark you created.
- If the article is behind a paywall, you will be redirected to a freemium version.

## Important Notes

- Use responsibly and in accordance with Medium's terms of service.
- This tool is intended for educational purposes only.
