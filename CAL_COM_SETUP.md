# Cal.com Integration Setup Guide

## Quick Setup Steps

### 1. Create Your Cal.com Account

1. Go to https://cal.com
2. Sign up for a free account
3. Complete your profile setup
4. Note your username (found in your profile URL: `https://app.cal.com/your-username`)

### 2. Create Event Types

In your Cal.com dashboard, create these event types:

- **Quick Connect** (15 minutes) - For brief introductions
- **Consultation** (30 minutes) - For project discussions  
- **Deep Dive** (60 minutes) - For strategy sessions

You can customize the names and durations as needed.

### 3. Update Portfolio Integration

The portfolio is already configured with `yashzode` as the Cal.com username. If your username is different:

#### Option A: Update in index.html

1. Open `index.html`
2. Find line ~18 (in the `<head>` section):
   ```javascript
   Cal("init", "yashzode", {
   ```
   Replace `"yashzode"` with your actual Cal.com username

3. Find line ~400 (in the booking section):
   ```javascript
   calLink: "yashzode",
   ```
   Replace `"yashzode"` with your actual Cal.com username

#### Option B: Keep "yashzode" username

If you want to use `yashzode` as your Cal.com username, make sure to:
- Sign up with that username on Cal.com
- Or change your Cal.com username in settings to match

### 4. Test the Integration

1. Open your portfolio locally or after deployment
2. Scroll to the "Schedule a Meeting" section
3. Click "Book Now" buttons or interact with the calendar
4. Verify that your Cal.com booking page opens correctly

### 5. Customize Booking Options

The portfolio has three booking cards. To match your Cal.com event types:

1. Open `index.html`
2. Find the booking cards section (around line 360)
3. Update the titles and descriptions to match your event types:
   ```html
   <div class="booking-card">
       <h3>Your Event Type Name</h3>
       <p>Your description</p>
       <button class="btn btn-secondary" onclick="Cal('inline', {layout: 'month_view'});">Book Now</button>
   </div>
   ```

## Embed Types Available

### 1. Inline Embed (Currently Used)
- Full calendar view embedded in the page
- Located in the booking section
- Shows month view by default

### 2. Popup via Button Click
- Opens booking in a popup/modal
- Triggered by "Book Now" buttons
- Good for quick access

### 3. Floating Button (Optional)
To add a floating button, add this code before `</body>`:

```html
<div id="cal-floating-button"></div>
<script>
    Cal("floatingButton", {
        calLink: "yashzode",
        buttonText: "Book a Meeting",
        buttonColor: "#6366f1",
        buttonTextColor: "#ffffff"
    });
</script>
```

## Troubleshooting

### Calendar Not Showing

1. **Check Username**: Ensure your Cal.com username matches exactly
2. **Check Script Loading**: Open browser console (F12) and look for errors
3. **Check Network**: Ensure you can access `https://app.cal.com`
4. **Check Event Types**: Make sure you have at least one event type created

### Calendar Shows but Can't Book

1. **Check Availability**: Ensure you've set your availability in Cal.com
2. **Check Event Types**: Verify event types are published and active
3. **Check Timezone**: Ensure your timezone settings are correct

### Styling Issues

1. **Container Size**: The calendar container has `min-height: 600px`. Adjust in `styles.css` if needed
2. **Responsive**: The calendar should be responsive. Test on mobile devices
3. **Custom CSS**: You can add custom CSS for the Cal.com iframe if needed

## Advanced Customization

### Custom Event Type Links

To link specific buttons to specific event types:

```javascript
// Instead of generic booking
Cal("inline", {
    elementOrSelector: "#cal-inline",
    calLink: "yashzode",
    layout: "month_view"
});

// Use specific event type
Cal("inline", {
    elementOrSelector: "#cal-inline",
    calLink: "yashzode/quick-connect",  // Replace with your event type slug
    layout: "month_view"
});
```

### Custom Colors

Cal.com respects your brand colors set in your Cal.com account settings. Update them in:
- Cal.com Dashboard → Settings → Appearance

## Support

- Cal.com Documentation: https://cal.com/docs
- Cal.com Support: support@cal.com
- Portfolio Issues: Open an issue on GitHub

---

**Note**: After making changes, clear your browser cache and test again to see updates.

