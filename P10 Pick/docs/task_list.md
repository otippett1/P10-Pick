# Task List – Carma (Builder View)

Each task below is derived from the Analyst’s final user stories in Specification 1.

---

### **T1 – Implement Smart Search Filters**
**Linked User Story:**  
_As a car owner, I want to search for parts using make, model, year, and trim so that I only see compatible results._

**Feature:** Discover Parts → Search Parts → Smart Filters  
**Description:** Build search inputs and logic that query listings based on make/model/year/trim combinations.  
**Acceptance Criteria:**  
- Search form contains dropdowns or autocomplete fields for make, model, year, trim.  
- Results dynamically update to show only compatible listings.  
- No matching results trigger a “No Parts Found” message.  
- Works consistently on mobile and desktop.

---

### **T2 – Create Used vs New Toggle**
**Linked User Story:**  
_As a buyer, I want to toggle between used and new listings so that I can compare price, quality, and availability across both markets._

**Feature:** Discover Parts → Used vs New Toggle  
**Description:** Add UI toggle and filter logic to separate used and new inventory.  
**Acceptance Criteria:**  
- Toggle present above search results.  
- Switching state refreshes results without page reload.  
- Selected filter persists when revisiting search page.

---

### **T3 – Display Seller Ratings & Reviews**
**Linked User Story:**  
_As a buyer, I want to see seller ratings and recent reviews so that I can evaluate trust before contacting them._

**Feature:** Discover Parts → Ratings & Reviews  
**Description:** Show average rating, number of reviews, and most recent comments per seller.  
**Acceptance Criteria:**  
- Ratings visible on all listings.  
- Clicking rating opens full review modal.  
- Data loads from verified purchase or community feedback table.  
- Empty state handled (“No reviews yet”).  

---

### **T4 – Add Report Listing Feature**
**Linked User Story:**  
_As a community-minded user, I want to report inaccurate prices or misleading listings so that the marketplace remains reliable and fair._

**Feature:** Discover Parts → Report Prices  
**Description:** Provide “Report” button on each listing with modal to flag issues.  
**Acceptance Criteria:**  
- Report form submits reason + optional comment.  
- Confirmation toast appears after submission.  
- Flags recorded in database with status = “pending.”  
- Admin view displays flagged listings.  

---

### **T5 – Build Follow Vendor System**
**Linked User Story:**  
_As a shopper, I want to follow specific vendors so that I receive updates whenever they post new items or discounts._

**Feature:** Shop Vendors → Follower System  
**Description:** Implement follow/unfollow functionality and notification triggers.  
**Acceptance Criteria:**  
- “Follow” button visible on vendor profile.  
- Follower count updates instantly.  
- User dashboard shows list of followed vendors.  
- New vendor posts send push/in-app notification.  

---

### **T6 – Create Verified Vendor Profiles**
**Linked User Story:**  
_As a vendor, I want to create a verified business profile with shop details and policies so that buyers recognize my store as legitimate._

**Feature:** Shop Vendors → Vendor Profiles → Verification Badge  
**Description:** Build vendor account type with verification workflow and editable business info.  
**Acceptance Criteria:**  
- Vendors can add logo, shop name, location, and policy text.  
- Admin can toggle verified = true → displays badge.  
- Verified vendors appear higher in search results.  
- Non-verified vendors restricted from posting discounts.  

---

### **T7 – Vendor Event Registration**
**Linked User Story:**  
_As a vendor, I want to register to table at upcoming car events so that I can promote my brand and meet customers face-to-face._

**Feature:** Shop Vendors → Event Participation / Sponsorship  
**Description:** Add event registration form and link vendor listings to event pages.  
**Acceptance Criteria:**  
- Vendors view event calendar with open registration.  
- Submitting form stores vendor ID + event ID + status.  
- Confirmation email or in-app alert sent.  
- Admin dashboard shows all event registrants.  

---

### **T8 – Community Posts & Builds**
**Linked User Story:**  
_As a new enthusiast, I want to browse community posts such as builds, tutorials, and tips so that I can learn and get inspiration._

**Feature:** Engage Community → Posts & Builds  
**Description:** Create feed displaying posts with images/videos and comment counts.  
**Acceptance Criteria:**  
- Feed loads paginated posts by recency.  
- Users can like, comment, and share posts.  
- Media uploads supported (photo/video).  
- Report/flag option available on each post.  

---

### **T9 – Join Groups & Themed Spaces**
**Linked User Story:**  
_As a user, I want to join topic-specific groups such as JDM, Muscle, or Euro so that my feed reflects my personal car interests._

**Feature:** Engage Community → Join Groups → Themed Spaces  
**Description:** Implement group categories and personalized feed filtering.  
**Acceptance Criteria:**  
- Users can join/leave groups.  
- Feed filters to joined groups.  
- Group pages show member list + recent posts.  
- Works seamlessly with mobile navigation tabs.  

---

### **T10 – How-To Q&A Module**
**Linked User Story:**  
_As a DIY learner, I want to post a how-to question with photos or video so that I can receive step-by-step help from others._

**Feature:** Engage Community → Posts & Builds / Q&A  
**Description:** Create Q&A post type separate from regular feed posts.  
**Acceptance Criteria:**  
- Q&A form includes title, description, and media upload.  
- Replies sorted by upvotes or recency.  
- Poster can mark “Best Answer.”  
- Notifications for new replies.  

---

### **T11 – Event Discovery System**
**Linked User Story:**  
_As an event-seeker, I want to discover nearby car meets within a chosen radius (5–200 miles) so that I can attend events that match my schedule and location._

**Feature:** Engage Community → Event Listings → Radius Filter  
**Description:** Implement event listing page with geolocation filtering.  
**Acceptance Criteria:**  
- Map or list view showing upcoming events.  
- Users can set radius slider and see filtered results.  
- Requires location permissions; fallback search by ZIP.  
- Event cards show name, date, distance, and “RSVP” link.  

---

### **T12 – Event Creation Form**
**Linked User Story:**  
_As an organizer, I want to submit an event with its date, location, and rules so that community members can discover and RSVP._

**Feature:** Engage Community → Event Listings / Event Creation  
**Description:** Build form to create new events and store data in Supabase.  
**Acceptance Criteria:**  
- Organizer can input name, description, date/time, location, rules.  
- Submitted event appears in public listings after approval.  
- Organizer can edit or delete own event.  
- Validation for required fields.  

---

### **T13 – Profile Editing & Customization**
**Linked User Story:**  
_As a user, I want to edit my profile with a photo, bio, and car details so that others understand my background and vehicle preferences._

**Feature:** Profiles → Bio & Picture Customization  
**Description:** Enable profile editing and file uploads for avatars and car images.  
**Acceptance Criteria:**  
- Edit page allows updating photo, bio, and car info.  
- Changes persist and appear instantly on profile view.  
- Image upload limits and validation enforced.  
- Mobile layout tested and responsive.  

---
