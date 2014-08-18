# jQuery.perpetualPosts

This plugin makes it easy to load in content as users scroll to the end of the page.

## Usage
### HTML
Create an anchor link linking to the content you want to inject on click or user scroll.
```
<a class="perpetual-posts" href="/post/post-to-load">Title of Post to Load</a>
```
### JavaScript
Load this code after the DOM has loaded.
```
jQuery('.perpetual-posts').perpetualPosts({
	sonar: true,
	callback: function (data) {
		// Manipulate data
		return data;
	}
});
```

### Events
The plugin broadcasts two events on the window. They are:
####posts.urlChanged
```
$(window).on('posts.urlChanged', function() {
	// the pages URL has changed and the new content has been loaded and displayed.
});
```
####posts.fetchingContent
```
$(window).on('posts.fetchingContent', function() {
	// new content is being requested. You can add a "loading" class to a placeholder here, for example
});
```
