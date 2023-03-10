# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
This project does NOT strictly adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.2.0] - 2021-08-26

### Removed

- Remove the need to use an invite code when registering.

### Fixed

- Fix content of Open Graph tags not being there in the pre-rendered HTML that Facebook's scraper sees.
- Fix sitemap `<lastmod>` value always being the current date.

## [2.1.6] - 2021-08-09

### Fixed

- Fix Open Graph tags not being implemented correctly.

## [2.1.5] - 2021-06-19

### Fixed

- Add meta descriptions to user and thread detail pages.

## [2.1.4] - 2021-06-18

### Changed

- Allow Google to again index most of the pages.
- Add dynamic thread and user detail pages back to sitemap.

### Fixed

- Fix FLoC opt-out header not getting returned on index page.

## [2.1.3] - 2021-05-31

### Added

- Add file thumbnails to user profile comments.

### Changed

- Opt out of Google FLoC.

### Fixed

- Fix bug of ordering not retaining on thread page after changing pages.
- Fix bug of comment file not clearing when closing the comment creation modal.
- Fix some thread links being shown as `@undefined` in user profile.

## [2.1.2] - 2021-05-12

### Fixed

- Don't show user's anonymous comments in their profile, and don't include them in user's comment counts.
- Fix iOS Smart App Banner not showing up.
- Attempt to improve the speed of loading a thread's comments.

## [2.1.1] - 2021-05-06

### Fixed

- Fix prod build not working.

## [2.1.0] - 2021-05-03

### Added

- Allow dropping files anywhere in home, search and thread pages and populate the thread
  creation form (home, search) and the comment creation form (thread page) with the file.
- Allow zooming in image viewer.
- Show thumbnails for comment files.

### Changed

- Allow setting either file or image in comments.
- Automatically open up the dialog that shows the allowed domains when a user
  tries to set an email with an invalid domain as the primary email. 

### Fixed

- Attempt to improve the speed of loading a thread's comments.
- Fix typo in author selection.
- Fix bug of clear comment file/image button not working.
- Show comments in user profile in chronological order.

## [2.0.2] - 2021-04-24

### Added

- Add support for adding comment files.
- Add support for using native sharing of Android devices.

### Changed

- Format all dates by minutes and not by days.
- Show reply buttons also for reply comments.
- Use the ordering parameters from URL.

### Fixed

- Fix safe are issues everywhere, make the image viewer more responsive.
- Fix swedish translations for views.
- Fix bug of avatar selection having incorrect texts.
- Fix UI strings for posting comments as anonymous.
- Add safe area inset to fix the spacing on the bottom of the landing page.
- Disable scrolling when the image viewer is displayed.
- Hide the bottom navbar on all error pages.
- Make the comment file link style consistent with other comment buttons.
- Improve the layout for the profile stats.
- Fix bug of the push notification signal handler logging an error for every activity.
- Fix bug of push notifications not working for users with multiple FCM devices.
- Fix bug of the invite dialog not closing when clicking the backdrop.

## [2.0.1] - 2021-04-19

### Added

- Show the avatar of the thread creator in the thread page.

### Changed

- Make the "best" thread sorting option take freshness into consideration.
- Lower the matching threshold of thread search.
- Replace star count with views in thread lists.
- Match the thread text font size with the comment texts.
- Add some indent on reply comments.
- Include share text in desktop Whatsapp links.
- Improve invite texts.
- Improve thread sharing texts.
- Improve profile sharing texts

### Removed

- Hide app store badges on native apps.

### Fixed

- Fix pagination working incorrectly.
- Fix bug of user link not working from thread page.
- Fix thread sharing links.

## [2.0.0] - 2021-04-19

### Added

- Allow users to delete their own anonymous comments.
- Allow users to set a backup email address. This needs to be verified with their primary email.
- Show comment creator score and badges on the comment card.
- Make the text search functionality return better results with incomplete search terms.
- Track user and thread views.

### Changed

- Hide most content from anonymous users.
- Only allow Finnish university email addresses in registration.
- Require invitation code in registration.
- Show a prompt on the home page for new users to invite friends.
- Completely redesign the landing page.
- Massively streamline the whole UI.
- Change courses into more generic threads.
- Give more score for comments and threads (old courses).
- Update guidelines, terms, and privacy policy to reflect the new feature set.
- Use skeletons instead of loading spinners for all tables.
- Use pages from API response data instead of query params.
- Rename "Community User" to "Anonymous Student".
- Improve sharing texts.

### Removed

- Remove dedicated material pages.
- Remove dedicated school pages.
- Remove trending page.
- Remove for-teachers page.
- Remove product updates.
- Remove blogs.
- Remove user marketing email settings.

### Fixed

- Fix issue where dark mode selection didn't persist.
- Order user's acquired badges by their tier.
- Fix constantly happening error when a user would have multiple mobile devices in use.

## [1.7.0] - 2021-03-24

### Added

- Add ability for users to track their progress of getting badges.
- Add info page for badges.
- Add support for push notifications with notification settings included in account settings.
- Add 'First Comment', 'First Course', 'First Resource', 'First Upvote', and 'First Downvote' badges.
- Show new badges in the activity feed.
- Send email and push notifications for acquiring badges.
- Add a product update about notifications and badge tracking.

### Changed

- Remove user's school from search filters when clicking on a subject link from course page.
- Disable email notifications by default for new and existing users.

### Fixed

- Fix a typo on the Finnish landing page.
- Fix issue where activity links that are comment replies cannot be clicked.

## [1.6.2] - 2021-03-14

### Changed

- Make all URL slugs immutable, except user slugs.
- Prevent trailing dashes (and other special characters) in slugs.
- Don't show the S3 filename when viewing a comment attachment.

### Fixed

- Fix error on course page which was caused by non-unique course slugs, by forcing them to be unique.
- Fix screen shaking on a Safari window that was 50% width of a 1080p screen.
- Make sure that the school filter is applied on the search page when coming to it by clicking a subject on a school page.

## [1.6.1] - 2021-03-11

### Fixed

- Fix URL slugs so that they're unique for all models.

## [1.6.0] - 2021-03-11

### Added

- Add page for managing email subscriptions.
- Add email notification settings to account settings.
- Add contact links to blogs for people who want to write blogs for us.
- Add contact links to product updates for people who have feature ideas for us.
- Add email subscription forms to product updates and blog posts shown for unauthenticated users - show links to account settings instead for authenticated users who have not subscribed to those.
- Add helper text to PDF viewer.

### Changed

- Improve email inputs on teacher page and email subscription forms - add loading indicator, disable field when submitting etc.
- Improve "snackbar" notifications - fix text overflow, adjust border radius.
- Change subjects label to optional in add course form.
- Make SA event from add comment page unique from other comments.
- Update marketing description.
- Use the same password fields for change password form that are used in registration form.
- Improve the button texts for returning from change password and my data pages back to account settings.

### Fixed

- Fix width for about page items.
- Fix comment query params.
- Fix duplicate results in trending suggestions.
- Fix subject link from course page to search.
- Fix home page layout on tablet screen sizes.
- Fix bug of links not working for school reply comment activities.
- Fix redirection from password reset page: logout -> login.
- Fix resource bottom navbar layout on small screen sizes.
- Fix Finnish translation for username helper text on registration form.
- Fix duplicates occurring in discussion suggestions.

## [1.5.5] - 2021-02-28

### Added

- Add a blog about the benefits of student organizations.

## [1.5.4] - 2021-02-20

### Fixed

- Fix bug of discussion not opening automatically from comment links on mobile.
- Fix broken width for search top navbar on mobile.
- Fix incorrect icon button colors on search page on mobile.

## [1.5.3] - 2021-02-16

### Added

- Add product update 15.2.2021
- Add trending link to desktop navigation.
- Add "reply" chip to reply comments showing in user profile.
- Add links to the latest blog posts in home page.
- Add link to own school discussion (if one exists) in home page.
- Add "noreferrer" attributes on all external links.
- Add account settings page that includes email, school, subject and email settings selection.
- Add continue button on account verification page under the "email sent" text.
- Add "verification required" template to prevent unverified users from accessing the add course and upload resource forms.

### Changed

- Tweak font sizes in landing pages once again to make them more responsive.
- Rename "Product" to "Skole" in footer again.
- Make the home page layout wider on laptop-sized screens.
- Make the footer layout width consistent with home page layout width.
- Move pages that were earlier under `/account-settings/*` path to root of the site.
- Improve miscellaneous translations.
- Change all course code references to plural form.
- Improve course page title when course has no course codes.
- Refer courses, resources, schools, school types, countries and cities with #-prefixes in the UI texts.
- Improve table rows by making the layout more responsive on mobile and including school links in course rows, course links in resource rows and dynamic links on comment rows.
- If comments have line breaks, only show the first line in table previews.
- Rename the URL `/upload-resource` to `/upload-material`.

### Fixed

- Fix bug of infinite loading screen on empty discussions.
- Fix links to school discussions and all reply comments from comment tables in trending lists and user profile.
- Fix bug of correct discussions not showing in school and resource pages.
- Fix bug of link buttons with "full width" not working - the widths broke in #369
- Fix bug of desktop navigation items not having the correct height - broken in #369
- Fix text wrapping for creator info texts in course, resource and comment tables.
- Fix links to user profile from comment tables.
- Fix CMD + click for all links.
- Fix bug of user avatar not working always when logging in with existing user saved in the device.
- Fix bug of autocomplete options not showing properly for fields support only one selection.
- Fix bug of comment deletion not showing for own comments.
- Fix bug of course menu button not showing on desktop.
- Fix bug of general form errors not working for various forms.
- Translate tooltip for opening autocomplete options and text for not having any options in autocomplete field.
- Fix various links having broken width due to custom link component.
- Fix spacing for avatar menu.
- Use consistent spacing and text alignment for all form texts.
- Fix bug of pre-filled school of user not working on add course form.
- Fix incorrect comment counts showing on discussions.
- Fix text overflow issue in long filenames on attachment viewer.

## [1.5.2] - 2021-02-11

### Fixed

- Fix infinite loading state on empty discussions.
- Fix links to school discussions from suggestions and user profile.

## [1.5.1] - 2021-02-10

### Fixed

- Fix typos and improve language.

## [1.5.0] - 2021-02-08

### Added

- Add school discussion.
- Add shortcut in home page to quickly add new comment to a relevant discussion.
- Allow users to include their messages in higher-level discussions:
  - In resources -> allow including messages in course discussion.
  - In courses -> allow including messages in school discussion.
- Add avatar thumbnails in comment tables.
- Show links to other discussions in comments if they have been included in those.
- Add navigation tabs for desktop layout.
- On course and resource pages, show a small score icon for non-verified users to make the score more clear.
- Add emojis on 404, 500 and offline pages.
- Add user's rank to top navbar on desktop.
- Add option for dark mode - save selection to browser.
- Add emoji to rank chip on profile.
- Add emoji to drawing mode header text.
- Add a link to the most recent product update on home page.
- Add 'Give us feedback' button to most Markdown pages.
- Add information about ranks to the score page.
- Add emojis on guidelines page headers.
- Add a blog about choosing a minor subject.
- Show author images on blog pages.
- Add author images on blog list.
- Add feedback link to footer.
- Pre-fill user's email in contact form.

### Changed

- Make upload materials button on course page more visible.
- Make add courses button on school page more visible.
- Rename the "no resources" text to "no materials" on course page.
- On mobile, only show info and actions button on top-right corner on course,
  resource and school pages and move all other shortcuts to the actions menu - no more duplicate actions.
- Add more spacing for the author selection button.
- Bump amount of visible comments and infinite scrolling amount to 20.
- When clearing autocomplete value, close the options automatically.
- Use hardcoded URL for resource page back button on desktop.
- Make all header titles slightly smaller.
- Use consistent header title style for course and resource pages with other pages.
- Make discussion header text more compact.
- Sort blogs and product updates in inverse chronological order.
- Hide desktop navigation on landing pages and loading screen.
- Optimize comment attachment images.
- Optimize main background image.
- Improve spacings on buttons on course and school pages.
- On user profile, use different tooltip when hovering own rank.
- Change autocomplete lists to show course codes in parenthesis.
- Hide app store badges from footer on landing pages where they were shown twice.
- Make sure blog images keep their aspect ratio.
- Improve contact form fields by fixing labels on optional fields and making subject and email fields optional.
- Don't log out users so quickly from the site.

### Removed

- Remove back button from desktop layout of all pages except resource page.

### Fixed

- Fix bug of drawing mode not working after first time on desktop.
- Fix exit drawing mode tooltip on resource page.
- Fix bug of unexpected error translations not working.
- Fix incorrect menu item icons for sharing and deletion actions.
- Fix bug of table row texts still overflowing on some screen sizes.
- Fix bug of pagination not working in school and user profile pages.
- Fix bug of avatar thumbnails not being rounded.
- Fix bug of avatar thumbnail not updating automatically after profile update.
- Fix vertical alignment on resource bottom navbar.
- Fix bug of correct bottom navbar content not showing for "owner" users on course and resource pages on mobile - the score icon was not visible, which is fixed now.

## [1.4.1] - 2021-02-02

### Changed

- Change the cover image for the 'trending content' product update.

## [1.4.0] - 2021-01-31

### Added

- Add product updates system and first update post.
- Add product updates link in the footer.
- Add preview thumbnails for comment attachments.
- Show loading dialog when sending new comments.
- Add support for automatic links in comments.
- Add app store badges in footer.

### Changed

- Allow filtering course autocompletion by the course code as well.
- Show bottom navbar on login, register and logout pages.
- Make footer column width match with home page content.
- Hide language button on non-translated pages.
- Show reply comments in top-level threads.
- Use scroll reveal/infinite scroll for comments to improve the rendering performance.
- Change social media links in footer to icons.
- Prevent showing Markdown images in comments.
- Make marketing description slightly larger on desktop on landing pages.
- Improve email body for shared links.
- Hide back button during loading screen on mobile.
- Combine the course name and code searches into one input.

### Removed

- Remove slogan from landing pages.

### Fixed

- Fix poor quality on PDFs.
- Fix translations for comment reply buttons and placeholders.
- Fix initial comment count for course and resource pages on mobile.
- Fix creator info alignment on table row layouts on tablet sizes.
- Fix broken WhatsApp sharing title from home page.

## [1.3.5] - 2021-01-28

### Changed

- Replace all emojis in menu items with material icons.
- Emphasize footer headers.

### Fixed

- Fix 500 error when requesting `sitemap.xml`.
- Fix vertical alignment for resource bottom navbar.
- Fix bug of created field not working in trending preview.
- Fix bug of comment links not working from profile.
- Fix text wrapping for tab labels on profile and remove emojis from them.

## [1.3.4] - 2021-01-26

### Changed

- Exclude reply comments from trending list.

## [1.3.3] - 2021-01-25

### Added

- Add consistent emojis for all header texts.
- Show user's comments in profile.
- Add current score and star count to course and resource headers on desktop.
- Add course to resource lists.

### Changed

- Slightly modify texts for register, verify account, logout, reset password pages.
- Change the text color for all header texts to a lighter shade.
- Change behavior of back button to take the user to landing page on first page view.
- Replace boring material icons with emojis in settings and about pages and in all dialogs.
- Make the layout for the pitch texts wider on teacher landing page.
- Change style for course, resource and comment tables.
- Reduce margin on Markdown paragraphs.
- Make the header texts on course and resource pages more responsive on desktop.
- Improve frontpage trending list.

### Removed

- Remove description meta tags from search page.

### Fixed

- Fix bug of tooltip not showing for settings button.
- Fix bug of votes, starred status etc. not loading properly on course and resource pages.
- Fix bug of resource PDF not loading properly from cache.
- Allow UTF-8 characters in my-data JSON file.
- Fix comment scores not getting calculated correctly.
- Fix issue where my-data download would return out of date information.

## [1.3.2] - 2021-01-21

### Fixed

- Fix analytics for landing and teacher pages.

## [1.3.1] - 2021-01-21

### Fixed

- Fix redirect after login.

## [1.3.0] - 2021-01-21

### Added

- Add suggested courses, resources and comments.
- Add app store links to teacher landing page too.
- Add blogging system and first blog about app store releases.
- Add about page that contains links to all info pages etc. (for teachers, contact, guidelines, score, values, blog, terms and privacy)
- Show back button on all settings pages on desktop.
- Add SA badges to values pages.

### Changed

- Make top navbar header text to truncate if it overflows.
- Move activity and starred pages in the root of the site.
- Change English texts for all "see all" buttons.
- Change login button on desktop to automatically redirect back to correct page.
- Update all course and resource tables to have a consistent style and modify their layout a bit.
- Make landing page texts more responsive to prevent wrapping to multiple lines.
- Update texts for teacher landing page.
- Enable app store links in landing page.
- Change href for Markdown reference link.
- Make back button always behave like the browsers back button.
- Send my-data downloads as links in the email instead of attachments.
- Change font from Roboto to Rubik.

### Removed

- Remove margins from Markdown paragraphs.
- Remove all table headers.

### Fixed

- Fix redirection from landing page to home page to not modify the navigation history.
- Fix bug of get started button showing on landing page on top right corner on desktop.
- Fix broken CSS property preventing text size being correct on Safari mobile.
- Fix bug of WhatsApp sharing link not opening externally.
- Fix URL for invite friends link.
- Fix title for invite friends link - remove colon.
- Fix paragraph margins for all Markdown content.
- Fix meta tags for all pages and locales.
- Fix miscellaneous emojis.

## [1.2.1] - 2021-01-16

### Added

- Add all courses and subjects from TUAS (=Turun AMK).

### Changed

- Use custom back buttons in login/register pages when navigating from landing page.
- Update marketing descriptions.
- Change all dialog header texts to H6 to save a bit more space.

### Fixed

- Fix course and resource scores not getting calculated correctly.
- Fix bug of author selection avatar not updating when choosing to comment as anonymous.
- Fix sharing links when current route has query params.
- Fix bug of back buttons missing on course and resource pages on mobile.
- Add support for disabling app store badges on native app.
- Fix paddings on bottom of the landing page on iOS PWA and native apps.
- Fix paddings on bottom of the for teachers page on iOS PWA and native apps.
- Fix text overflow for dialog headers.
- Fix spacings for backdrops so that they fill the entire screen.
- Fix inconsistent font size on Safari.

## [1.2.0] - 2021-01-14

### Added

- Add link to landing page in the footer.
- Add new "next step" item with dynamic content on home page based on the actions the user has taken.
- Add star count to course and resource info dialogs.
- Add back buttons for basically all pages both on desktop and mobile.
- Add landing page for educators.
- Add handling for an edge case when user navigates to verify account page as not logged in and without token.
- Add a next step item on home page for adding school and subject.
- Update left column header on footer and add a link to "for educators" page.
- Add indicator for unread notifications on both mobile and desktop.
- Add initial versions/drafts for score reference, company values and community guideline pages.
- Add footer links for the new pages.
- Add Software Engineering subject.
- Add links to guidelines in course creation and resource upload pages.
- Add link to send materials via email on upload resource page.
- Add date field to upload resource form.
- On upload resource page, show email link to send materials manually as a batch via email.
- Redirect authenticated users from landing page to home page.
- Prefill user's school on upload resource and add course pages if no other school is provided as a query parameter.

### Changed

- Prevent redirection to landing page from pages that do not require authentication.
- Enable drawing mode on PDF viewer.
- Rename "draw mode" to "drawing mode" in PDF viewer.
- Use shared "unexpected error" notification for all edge cases such as voting errors etc.
- Change casing for words in quotes in terms and conditions.
- Refactor terms and privacy pages to static pages generated from Markdown at build time.
- Change link style in all Markdown pages and comments to consistent red.
- Change spacings for all dialogs that are lists such as settings, sharing dialogs etc.
- Hide settings toolbar from pages that have nothing to do with settings such as starred, terms and privacy pages.
- Use more descriptive title for discussion header to indicate the amount of comments on desktop.
- Change all autocomplete fields to re-fetch the data on every keystroke.
- On resource page on mobile, instead of a blank bottom nav bar for non-verified users on discussion tab, show the default bottom nav bar instead.
- Update helper text for register form's username field.
- Update texts for landing page.
- Update next steps texts on home page.
- Change layout for all pages that were previously using the settings layout except for edit profile, change password, my data and delete account pages.
- Hide terms, privacy and contact links from the settings menu on desktop.
- Make avatar bigger on user profile on desktop.
- Change activity tooltip to show the amount of unread activities.
- Move language button from footer to always be on top-right corner on desktop.
- Update Swedish locale for for-educators page.
- Make content of all static Markdown pages slightly narrower.
- Make bottom and top nav bars slightly thicker on mobile mostly in order to have more space for the unread activity indicator.
- Render "login required" and "logout" content directly on pages and remove redirection to another page.
- Improve buttons and button texts register and login pages.
- Change landing page URL to the root of the site and home page under `/home` URL.
- Change the marketing description to even shorter one.
- On mobile, show language button on top-right corner for all pages that do not have custom content there.
- On home page, on mobile, for anonymous users, show a small launch icon button in the top-left corner that takes the user to the landing page.
- Show "file selected" text in the middle of the drop zone and as the file selection button text on mobile.
- To save space in the top nav bar, show login/register buttons only up from 960px.
- Hide get started button for authenticated users in footer.
- Change all error layouts (server error, offline, 404) to have a responsive and consistent layout.
- Change locales for all error pages and layouts to shorter ones that they fit well on mobile screens.
- Change URL for reset password page from `/account/reset-password` to `/reset-password`.
- Add reset password page to indexable pages.
- Always use English headers for privacy and terms pages.
- Change mail address in privacy page to link.

### Removed

- Remove confirm login and confirm logout pages.
- Remove all automatic redirects on on landing page and login etc.
- Remove description meta tag texts from all pages that are not indexed.
- Hide logo on student landing page on mobile.
- On logout page, show login, register, get started and for teachers button after logout.
- Show login button on register page on top right corner on desktop.
- Show register button on login page on top right corner on desktop.
- Show dynamic texts (course name, resource title, school name) as info dialog headers on course,
  resource and school pages and remove that info from the actual dialog content.

### Fixed

- Fix the misaligned screenshots in drawing mode.
- Fix bug of comment count not showing on course and resource pages.
- Fix sharing link for comments.
- Fix links for next steps on home page.
- Fix bug of back buttons having incorrect color on mobile.
- Fix bug of bottom nav bar not showing on home page.
- Fix bug of activity menu button not showing on activity page on mobile.
- Fix bug of backend file errors not showing on upload resource form.
- Fix language button size on mobile.
- Fix authentication synchronization so that logging out from all tabs works from all pages.
- Fix navbar positioning on search page on Safari mobile.
- Fix bug of activity page header not showing on mobile.
- Fix bug of UI indicating that the user is still logged in on logout page (could be noticed only on mobile).
- Fix avatar thumbnail not showing.

## [1.1.1] - 2021-01-02

### Changed

- Make username and email case-insensitive on login.
- Make email case-insensitive on forgot password form.

## [1.1.0] - 2021-01-01


### Added

- Add "next steps" section to home page.
- Add contact us links to register form, add course form, search form and home page.
- Slightly modify miscellaneous helper texts and locales.
- Improve error messages by adding dedicated locales for error messages of unstar and vote removal actions.
- Add every single country of the world to the country selections.
- Add a `sitemap.xml` and a `robots.txt`.

### Changed

- Use regular tab panels instead of swipeable views for all tab views.
- Add more detailed header texts for info dialogs of course, resource and school pages.
- Improve PDF viewer's pinch gestures which had an offset to the left. Now the pinch gesture works perfectly.
- Move PDF page number input under the PDF viewer.
- Show default bottom nav bar for non-verified users on course page.
- On mobile, do not render the "add course to this school" button on course page at all.
- Bump PDF viewer's max zoom to 5.
- Implement a regular text/Markdown editor instead of using draft.js editor.
- Make avatars on comment cards bigger.
- Fix all other avatar thumbnails so that they match with all other icons in size.
- Show comments that scroll under the comment reply button on mobile.
- Unify spacings of several headers and dialog headers.
- Change the layout for course and resource pages slightly to allow more space for the discussion card.
- Make all card headers slightly smaller.
- Show send button on top-right corner of comment creation modal.
- Add slight borders around scroll containers to distinguish them better.
- Remove extra padding from the left of resource table body.
- Improve miscellaneous locales.
- Add tooltips for removing upvotes/downvotes.
- Hide rotate button on mobile when on discussion tab on resource page.
- Use consistent borders in all card headers.
- Allow all forms to have slightly wider fields.
- Allow submitting comments with enter key on desktop.
- Move submit button for sending comment next to the text field on mobile.
- Make avatar on author selection button larger.
- Make spacings for all dialog headers more consistent with other spacings on the app.
- Enable text selection on desktop.
- Allow more space for all dialogs that are not full screen.
- Update locales for all confirmation modal texts.
- Reorder resource menu actions.
- Add a minimum height and increase padding for the not found element.

### Fixed

- Fix vote indicators not showing own vote's status on course and resource pages.
- Fix positioning for comment actions button on reply comments without attachments.
- Fix positioning for create comment button on mobile.
- Fix z-index issue for bottom nav bar causing some elements to overlap it.
- Make sure school page header is centered.
- Fix positioning for create comment button on mobile.
- Fix downloaded my data JSON having user's created and modified values being swapped.
- Fix remaining overflow issues for PDF viewer.
- Fix typo in landing page.
- Fix scrolling behavior on tables.
- Fix bug of having double scroll bars on some tables and discussion tab at least on Safari mobile.
- Fix vertical alignment for no comments text.
- Fix home page sharing menu header.

## [1.0.0] - 2020-12-18

### Added

- Add `account/my-data` page for GDPR user data requests.
- Add labels for rank and badges on profile page.
- Make verification and password reset URLs link to translated pages.
- Allow uploading files and selecting images on mobile Safari.
- Add short pitch section about Skole on landing page.

### Changed

- Update privacy policy.
- Make any object deletion be completely permanent.
- Change Google Analytics to Simple Analytics.
- Change URL for course creation page to `/add-course`.
- Improve rendering of long form field errors.
- Change password minimum length to 10 characters.
- Don't allow too common passwords.
- Don't allow entirely numeric passwords.
- Don't allow passwords that are too similar to user's username or email.
- Sort subjects and schools alphabetically.
- Improve miscellaneous translations.
- Prevent compressing attachment and avatar images that are smaller than the allowed limit.
- Make comment author selection into a clickable button.
- Make rich text editor icon button sizes match the sizes of comment icon buttons.
- Fix translation for error message of password being too similar to the email.
- Don't require a verification for sending a password reset email or resetting password.
- Don't allow special characters in usernames.
- Update font weight, color and spacing for completed profile strength steps.
- Add more spacing between the texts on profile page.
- Don't use 'noreply' email addresses, instead encourage users to reply to emails.
- Prevent submitting comments from return key on mobile/tablet.

### Removed

- Don't show the 'see all' share option button when on Desktop.
- Remove code-block option from the rich text editor.
- Hide top navbar search on landing page.

### Fixed

- Fix issue where autocomplete fields could return duplicate results.
- Fix resource type field not showing any choices on first load of upload-resource page.
- Fix inconsistent spacing of message info icons and buttons.
- Fix bug of share menu's copy link action not working.
- Fix bug of resource creator not showing in user profile under the created resources.
- Fix bug of subject and course lists not being rendered on school page.
- Fix issue where course, resource, and comment deletion would not delete the object properly.
- Fix issue where uploaded resource files could lose almost all of their text.
- Fix text alignment of dialogs on desktop.
- Fix overflow issue of rendering profile badges.
- Fix spacing issue of profile strength steps etc. on profile page on mobile.
- Fix sharing locales for resource page.
- Fix rendering quotes in comments.
- Fix rendering strike through in comments.
- Fix bug of resource creator not showing on course page.
- Fix bug of bio not showing on desktop at all.
- Fix bug of some profile info labels having capital casing and incorrect spacing on some screen sizes.
- Fix slogan text on get started page.
- Fix avatar dialog buttons not working correctly.
- Fix main background image stretching weirdly.
- Fix overflow issues on footer links.
- Fix sharing links to WhatsApp and Telegram.

## [0.17.1] - 2020-12-10

### Changed

- Add content on privacy policy and terms pages.
- Show wider text content on terms and privacy pages.
- Update spacings for comment buttons.
- Translate all emails.

### Fixed

- Fix email sharing link.
- Miscellaneous locale fixes.
- Fix issue with long texts of comments overflowing.

## [0.17.0] - 2020-12-07

### Added

- Add custom Instagram-like sharing menu for more user-friendly sharing options.
- Add option for authenticated users to post as anonymous users.
- The username and avatar of the account making the comment in the comment creation form.
- Add keywords and Twitter meta tags to improve SEO.

### Changed

- Improve sharing titles and texts.
- Make bottom border of a top-comment of a thread slightly narrower.
- Make avatar thumbnails slightly smaller.
- On top comments in threads, show the reply count directly in the comment like in all the top-level comments.
- Align vote-buttons of comments vertically always on center like in Model.
- Make the max height of the rich text editor more responsive.
- Change the layout for all dialog headers to a bit denser so that the center content has more space.
- Hide top nav bar search field for 404 page.
- Change uncompleted profile strength steps into clickable links.

### Fixed

- Fix bug of rich text editor pushing itself away from the viewport when stretching against the comment attachment.

## [0.16.8] - 2020-12-03

### Fixed

- Miscellaneous UI fixes.

## [0.16.7] - 2020-12-03

### Added

- Add miscellaneous helper texts for form fields.

### Changed

- Use SVG icons for language flags.
- Instead of showing disabled vote and star buttons for anonymous/unverified users in course/resource pages, completely hide the buttons on mobile.
- Disable "mark all as read" action in activity page if user has no actives.
- Improve miscellaneous locales and helper texts.
- Make all forms a bit wider on extra wide screens.
- Remove placeholder notification settings from edit profile page.
- Change the resource upload form flow to the following:
  - By default, only show the following fields: title, type, school, file
  - After school field is populated, collapse in the course field under the school field. Note that this field already contains only options filtered for the selected school. This way we can force the user to pick the course from only one school at a time.

### Fixed

- Fix bug of being able to select duplicate values for auto complete fields that allow selecting multiple values.
- Fix bug of comment modal not opening manually, if clicking on an activity in the activity preview modal and users already in the destination page.

## [0.16.6] - 2020-11-28

### Changed

- Update miscellaneous texts and translations.
- Use Markdown for rendering comments and bio field in user profile.
- Change layout to show the desktop layout for all devices 960px wide.
- Disable search field for 500/offline pages.
- Only pre-fill users selected school in search page.

### Fixed

- Fix overflowing texts of comments.
- Fix bug of top-level comments not being updated after sending reply comments.
- Fix bugs regarding the form initialization on search page, upload resource page and possible on other pages too.
- Fix bug of static assets such favicon not working on other pages except the home page.

## [0.16.5] - 2020-11-27

### Changed

- Use global loading screen in fewer places and use smaller loading indicators for individual components instead.
- Add animated logo to the global loading screen.
- Update social media links to be only text.
- Enable search box in the nav bar for anonymous users.
- Allow selecting text from PDF files.
- Move gray background lower on home page.
- Disable grouping by resource type in resource lists.
- Show the type of every resource in resource lists.

### Removed

- Remove FAQ page.
- Remove About page.

### Fixed

- Fix name label on contact form.
- Fix bug of user profile form not updating.
- Fix delete course menu item icon clicking not working.
- Fix upload resource form link to contact.
- Fix school detail URL.
- Fix activities caused by anonymous user comments.
- Fix bug of rich text editor omitting last character from comments.
- Fix links not being clickable in account verification and password reset emails.
- Fix error which occurred when uploading any files.
- Improve frontend translations.
- Fix attachment preview stretching the images.

### Security

- Add protection against CSRF attacks.
- Remove exception details from backend responses.

## [0.16.4] - 2020-11-12

### Changed

- Change overall scrolling behavior and scrolling logic for tables.
- Make rich text editor buttons smaller.
- Improve typings for PDF related components.

### Fixed

- Fix paths for link-tags in the HTML head.
- Fix positioning for nprogress bar.
- Fix positioning for dialogs and backdrops.

## [0.16.3] - 2020-11-11

### Changed

- Allow navigating back from "confirm login/logout" pages.
- Remove error handling for logging out.

### Fixed

- Fix loading states between automatic redirects to prevent pages from flashing.
- Fix bug of user profile not being reset after logging out.

## [0.16.2] - 2020-11-09

### Fixed

- Prevent the API from allowing comment attachments from non-verified users.
- Fix comment deletion for non-verified users.
- Fix bug of account verification page being blank for verified users.

## [0.16.1] - 2020-11-08

### Added

- Display number of downloads for resources.

## [0.16.0] - 2020-11-06

### Added

- Add pagination to all lists that display courses, resources or subjects.
- Add social media links in the footer.
- Add helper text for the title field in the upload resource form.

### Changed

- Change the designs for landing and home pages
- Re-implement translations with a lighter `next-translate` library and built-in next.js localized routing.
- Use a dedicated query for the activity preview menu.
- Use nprogress instead of the default loading screen for page transitions.
- Refactor misc. typings for cleaner code.
- Update Next.js to latest v10.0.1 version, implement the new `next/image` component for most images.
- Improve GraphQL API documentation shown in GraphiQL.
- Make comment cards more reasonably sized.
- Move the link to delete account button to edit profile page.

### Fixed

- Fix bug that prevented submitting the register form.
- Fix layout issues in resource page and some settings pages.
- Fix bottom navbar navigation and Finnish translations when not authenticated.
- Potentially fix bug of top-level comments not being reset when changing routes.
- Fix mutation payloads according to the latest backend schema.
- Fix layout for user profile when viewing other users' profiles.

## [0.15.1] - 2020-11-01

- Fix CircleCI pipeline errors.

## [0.15.0] - 2020-10-31

### Changed

- Deploy and manage the whole AWS infra with terraform.
- Clean the metadata of all uploaded files.

## [0.14.1] - 2020-10-12

### Added

- Add a login confirmation page that is shown to the user before automatically redirecting to login page.

### Changed

- Add resource count to profile tab labels.
- Simplify tooltips for voting own content - use the same "You cannot vote on your own content" for courses, resources and comments.
- Disable draw mode feature temporarily - for mobile devices, hide the entire button.
- Use a lighter color for community user in comments.
- Remove success notification after creating a comment.
- Improve URL input for rich text editor.
- Hide attachment button for anonymous and non-verified users on mobile.
- Improve spacing and alignment for course table items.
- Hide profile strength stepper if all steps have been completed.
- Show course/resource count on profile tab labels.
- Make all icons and icon buttons slightly bigger.
- Bump max file size to 10Mb when uploading resources.
- Add option to navigate to home from logout and login/register pages.

### Fixed

- Fix bug of created resources not showing in profile.
- Fix bug of anonymous users being able to click on vote/star buttons.
- Fix bug of confirmation modal not showing when deleting a comment.
- Fix spacing and overflow issues for rich text editor.
- Fix navigation logic to user profile from bottom nav bar when not logged in.
- Fix weird overflow issue occasionally present on mobile iOS, affecting entire container/layout.
- Fix overflow issue on profile username and title fields.
- Fix infinite loading state bug on some forms.
- Fix navigation on bottom nav bar for anonymous users.
- Fix layout on all settings pages.
- Fix reply comment button text.

## [0.14.0] - 2020-10-10

### Changed

- Show comment and resource counts, and the creator of the course in all course lists.
- Refine the border radius of all UI elements a bit.

### Fixed

- Fix showing user's starred courses and resources on starred page.

## [0.13.0] - 2020-10-10

### Added

- Group resources by resource type in lists.

### Changed

- Improve developer documentation.
- Restructure static assets (images).
- Improve miscellaneous locales.
- Make dialogs more responsive - no more side-opening drawers on desktop.
- Remove redundant top-level dependencies.
- Add labels to bottom navbar.
- Create custom drop zone for file uploads.
- Replace `formik-material-ui` with custom form fields.
- Use MUI's built-in media queries instead of a custom solution.
- Simplify layout for settings page other reusable templates.
- Improve labels and placeholders for all form fields, remove redundant input adornments that look weird on iOS.
- By default, show footer in viewport on desktop.
- Improve "not found" screens with more descriptive texts, icons and call-to-action links.
- Redesign and implement landing and home page.
- Slightly redesign profile page, improve profile strength stepper (always show completed steps first).
- Change theming with e.g. rounded corners and other misc. overrides to default MUI components.
- Remove NProgress - show regular loading screen instead
- Improve all tables for better compatibility and hover effects etc.
- Replace `moment.js` with `day.js`.
- Make most content pages public (home, search, course, resource).
- Allow commenting for non-logged users but prevent them from adding resources.
- Prevent autocomplete fields from making massive queries. Instead, fetch initial data and re-fetch when user types in more characters.
- Make headers slightly bigger.

### Fixed

- Fix client-side logout error.
- Fix bug that caused form error when logging in with different credentials as an existing user.
- Replace all styled-components styles with MUI's own CSS in JS.
- Fix error handling for all mutations with the latest backend version.
- Fix status bar style on iOS.
- Fix miscellaneous iOS bugs.
- Fix HTML lang-attribute.
- Fix create comment button positioning.
- Fix bug of bottom navbar not showing non-authenticated users.
- Fix lang-attribute for HTML-document.
- Use client-side data fetching for all dynamic pages - fix translation bug.
- Fix bug of theme overrides not being applied and thus miscellaneous UI elements looking weird.
- Fix miscellaneous UI bugs.
- Fix translations on user profile by using client-side data fetching.
- Fix miscellaneous locale typos.
- Fix avatar thumbnail sizing on mobile.
- Fix PDF viewer overflow issue preventing border radius from showing.
- Fix bugs of dialogs toggling on/off from random clicks.
- Fix school detail overflow issue.

## [0.12.2] - 2020-09-12

### Fixed

- Correctly log out the session after an account deletion.
- Fix rich text editor submit button.

## [0.12.1] - 2020-08-17

### Changed

- Change file input for mobile devices on upload resource page.

### Fixed

- Fix bug causing resource draw mode to clash with swipeable views.
- Fix all file upload fields to allow uploads using either camera or device storage.
- Fix bug causing edit profile page to crash when uploading new avatar.
- Fix bug that caused other search params to disappear when entering course name on mobile search.
- Fix bug that caused comment thread to open when voting on top-level comment.
- Fix bug that caused comment thread to open when clicking on comment actions drawer.
- Fix bug that caused incorrect tooltips to show in various places when user has not verified his account.
- Fix incorrect score counts showing on course listing.

## [0.12.0] - 2020-08-16

### Added

- Add initial version of rich text editor for course and resource discussion.

### Changed

- Disable offline functionality for home page.
- Change loading screen to take up full screen on desktop.

## [0.11.0] - 2020-08-12

### Added

- Add "best" sorting option for courses, it's used by default.

### Changed

- Disable backend's spammy permission error logging.

### Removed

- Remove option to sort courses by ascending score.

### Fixed

- Fix error which prevented voting a course.
- Fix error which prevented commenting to a course.

## [0.10.2] - 2020-08-10

### Fixed

- Minor UI tweaks.
- Fix frontend CircleCI env variables.

## [0.10.1] - 2020-08-09

### Fixed

- Fix CircleCI pipeline errors.

## [0.10.0] - 2020-08-09

### Changed

- Revert back to using a server for frontend hosting.
- Improve the about page.
- Improve meta tags.
- Allow non-logged in users to view courses, resources, and user profiles.
- Don't allow non-verified users to create resources or courses.

## [0.9.11] - 2020-08-08

### Security

- Only allow JWT cookie on HTTPS.

## [0.9.10] - 2020-08-08

### Fixed

- Allow Vercel preview build to use backend JWT cookie.

## [0.9.9] - 2020-08-08

## Fixed

- Fix service worker registration.

## [0.9.8] - 2020-08-08

### Added

- Add custom offline page for all pages that require communication with backend.
- Add "Back to profile" button in edit profile page.
- Add default title and description meta tags for pages.

### Changed

- Change registration to three-step flow.
- Change PWA so that content is refreshed automatically.

### Fixed

- Fix meta tags for loading screens.
- Fix miscellaneous locales.

## [0.9.7] - 2020-08-07

### Fixed

- Fix bug which prevented accessing Badge model from the admin.

## [0.9.6] - 2020-08-06

## [0.9.5] - 2020-08-06

## [0.9.4] - 2020-08-06

### Fixed

- Fix ECS task definition memory allocation.

## [0.9.3] - 2020-08-06

### Security

- Use different `CORS_ORIGIN_REGEX_WHITELIST` for prod and QA for extra security.

## [0.9.2] - 2020-08-06

### Changed

- Use rolling backend updates for QA also.

## [0.9.1] - 2020-08-06

### Fixed

- Fix AWS task definition issues.
- Fix CircleCI pipeline errors.

## [0.9.0] - 2020-08-06

### Changed

- Deploy frontend as static files.
- Change Cloudmersive PDF converting to the backend.
- Simplify QA/prod env variables.

## [0.8.1] - 2020-08-03

### Added

- Add custom login for existing users.
- Add custom offline page.

### Changed

- Transform frontend into completely serverless.

### Fixed

- Fix authentication issues causing redirects.

## [0.8.0] - 2020-08-03

### Added

- Add new Bachelor rank between Mentor and Master.

### Changed

- Increase the amount of needed score for ranks Master and up.

### Fixed

- Make admin and frontend authentications not clash with each other,
  thus making it possible to use them simultaneously

## [0.7.1] - 2020-08-02

### Fixed

- Fix port issue which prevented frontend from starting at all.

## [0.7.0] - 2020-07-31

### Added

- Add small resistance animation to swipeable views.
- Add get started page.
- Add logout page.
- Add confirm logout page when an authenticated user tries to access login/register pages.
- Add profile strength indicator to user profile.

### Changed

- Change all tabs to swipeable.
- Change course page and create course pages so that course now supports multiple subjects.

### Fixed

- Fix sharing comments.
- Fix locale typos.

## [0.6.2] - 2020-07-13

### Changed

- Added swipeable views for all tabs.
- Improve about page and add link to feedback.

### Fixed

- Fix bug of displaying error after cancelling share.
- Fix loading icon lagginess.
- Fix bug of being able to see edit profile and starred item buttons on other user's profiles.
- Fixed authentication on all public setting pages.

## [0.6.1] - 2020-07-12

### Fixed

- Fix bug of displaying PDF viewer screenshot at incorrect size/cutting out areas.
- Fix bug of not centering horizontal scroll when zooming in/out on PDF viewer.
- Fix bug of not displaying correct cursor on PDF viewer when holding down CTRL key.
- Potentially fix CORS error related to printing PDF file.

## [0.6.0] - 2020-07-10

### Added

- Add activity feed that shows notifications for comment replies, course and resource comments.

### Fixed

- Fix bug that prevented user from being actually logged out.
- Fix bug that occasionally prevented user from logging in and setting client-side cookies.

## [0.5.0] - 2020-07-07

### Fixed

- Fix authentication bug that led redirecting to login screen randomly.
- Fix miscellaneous spelling errors and translations.
- Fix bug of displaying duplicate comments in comment sections.

### Added

- Add attachment name to attachment viewer toolbar.
- Add draw mode to PDF viewer that allows user to take screenshots from document.

### Changed

- Make complete re-implementation to PDF viewer, show all pages at once as a scrollable document.
- Update designs by using fewer different fonts, add different shades of theme colors, update modal designs.

## [0.4.10] - 2020-05-18

### Fixed

- Fix contact form email sending.

## [0.4.9] - 2020-05-18

### Fixed

- Fix user agent matching to fix layout prediction.
- Fix authentication issues.

## [0.4.8] - 2020-05-11

### Added

- Add FAQ page.
- Add monorepo scripts for frontend lint and type-check.

### Changed

- Disable votes, stars and comments for unverified users in frontend.
- Improve error message upon unsuccessful registration email.
- Don't show error when sharing menu is dismissed.
- Updated landing page design.
- Changed all frontend dependencies to strict versions.

### Fixed

- Fix typo in account verification.
- Fix persisting notification after page changes.
- Fix links from school detail.
- Fix auto complete fields with empty content.
- Fix search bar clearing on mobile when blurred.
- Fixed GraphQL code generation config.

## [0.4.7] - 2020-05-04

### Changed

- Backend AWS SES changes.

## [0.4.6] - 2020-05-04

### Changed

- Small AWS changes.

## [0.4.5] - 2020-05-03

### Fixed

- Fix backend SES configuration issue.

## [0.4.4] - 2020-05-03

### Fixed

- Send email through SES to avoid blocking issues.

## [0.4.3] - 2020-05-03

### Fixed

- Use email host user for auth emails.

## [0.4.2] - 2020-05-03

### Added

- Prompt user about updated content and re-register service worker.

## [0.4.1] - 2020-05-02

### Fixed

- Fix error in backend createsuperuser command.
- Fix syntax error in initial data fixtures.

## [0.4] - 2020-05-02

### Added

- Add search navbar to search page.
- Add school and subject selection to user profile and register form.
- Add badges and ranks for users.

### Changed

- Improve profile page.
- Made graphql queries for non-user generated content public.

### Removed

- Remove user listing page.

### Fixed

- Fix form getting validated in back-end before authentication check was done.

## [0.3] - 2020-04-27

### Added

- Add account verification via email.
- Add password reset via email.

### Changed

- Logging in with email or username is back.

### Fixed

- Disable enter key sending for mobile devices.
- Fix switching between tabs after creating a new comment makes the comment disappear.
- Fix header overflow being too small on mobile.
- Don't always show the same file when opening a resource.
- Fix going back in resource view.

### Security

- Improve Docker security by using non-root users in containers.

## [0.2.4] - 2020-04-19

### Fixed

- General bug fixes from alpha users' feedback.

## [0.2.3] - 2020-04-18

### Fixed

- User profile update.
- Other misc improvements.

## [0.2.2] - 2020-04-10

### Added

- Add automatic user refreshing every 25 minutes.
- Improve avatar changing feature.

### Changed

- Improve profile page.

## [0.2.1] - 2020-04-09

### Added

- Add health check API.

### Changed

- Translate initial data.
- Improve PDF viewer.

### Fixed

- Fix iOS pagination.
- Fix info modal creator info.

## [0.2.0] - 2020-04-07

### Added

- Add user avatar to bottom navbar.
- Add email configuration for contact form.
- Add model translations.

### Changed

- Store user information in local storage to reduce the amount of server requests.
- Make email an optional field and do not require it when registering new account and when updating profile.

### Removed

- Remove redundant frontend dependencies and secondary PDF viewer.

### Fixed

- Fix bug of 'Edit Profile' button showing on other users' profiles.
- Fixes to backend translations.

## [0.1.0] - 2020-04-05

### Added

- Deploy initial version.
