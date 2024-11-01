**Custom Page Feature of The Planning Center Software**

Table of Contents

**1\. [Introduction](#introduction)**

   - [Purpose/Objective](#purposeobjective) 

   - [Product Overview](#product-overview)

**2\. [In Depth Testing Approaches and Strategies](#in-depth-testing-approaches-and-strategies)**

   - [Functional Testing](#functional-testing)

   - [Non-Functional Testing](#non-functional-testing)

   - [API Testing](#api-testing)

   - [End-to-End Testing](#end-to-end-testing)

   - [Regression Testing](#regression-testing)

**3\. [Test Environments](#test-environments)**

   - [Devices and Browsers](#devices-and-browsers)

   - [Testing Software and Tools](#testing-software-and-tools)

**4\. [Team Communication and Version Control](#team-communication-and-version-control)**

**5\. [Examples of Key Testing Scenarios & Challenges](#examples-of-key-testing-scenarios--challenges)**

   - [Custom Page Creation](#custom-page-creation)

   - [Block Types](#block-types)

   - [Planning Center Blocks](#planning-center-blocks)

   - [Publishing a Page](#publishing-a-page)

   - [Performance and Scalability Challenges](#performance-and-scalability-challenges)

   - [Cross-Platform Consistency Challenges](#cross-platform-consistency-challenges)

   - [Multi-language Support Challenges](#multi-language-support-challenges)

**6\. [Prioritized Test Plan for Custom Pages Feature](#prioritized-test-plan-for-custom-pages-feature)**

   - [Sprint 1](#sprint-1)

   - [Sprint 2](#sprint-2)

**7\. [Conclusion](#conclusion)**

**8\. [Resource Links](#resource-links)**

1.  Introduction #introduction

**Purpose/Objective of this Test Plan** 

This test plan document outlines the testing strategy and approach for The Planning Center's Custom Pages feature. It provides a structured plan to test the application's functionality and ensure its reliability and quality. This test plan covers the types of testing to be conducted, key scenarios, objectives, and challenges when testing the Custom Pages feature of The Planning Center's software. 

It will begin with in depth examination of the different approaches and strategies, followed by suggested testing environments, software and tools. Then proceeding into detailed examples of key testing scenarios and challenges concluding with a prioritized test plan targeting crucial areas of focus within a 2 sprint timeline.   

**Product Overview**

The Planning Center offers a suite of subscription-as-a-service software project management tools designed for church congregations to enhance their communities. They provide a wide collection of tools to help manage ministries and religious communities, such as event calendars, donation trackers, communication groups, registration tracking forms, custom web and mobile page publications, and much more. This application is available for mobile and web users and is designed to seamlessly connect admins and users within the same environment.

The Custom Pages feature allows churches to create a web/mobile app for their own church domain, customized with pictures, videos, and links. It provides creators with an easy, no-code way to drag and drop and design a custom page. In addition to allowing creators to add original text, links, and media, there is also integration with other Planning Center products that can be featured on the page.

2\. In Depth Testing Strategy

**Functional Testing**

_Functional testing will ensure that the application's features perform as expected, based on the defined requirements. Both manual and automated testing will be conducted, focusing on the following components:_

**\- Creating a New Page:** Test that users can successfully create a new custom page. 

**\- Adding Content:** Ensure that users can add text, images, videos, social media links, and section dividers with various content types. 

**\- Drag-and-Drop Functionality:** Verify that the drag-and-drop feature for adding and moving content works seamlessly. 

**\- Third-Party Content Integration**: Test the embedding of external content, such as YouTube videos or map APIs, to ensure proper functionality. 

**\- Integration with Planning Center Products:** Validate that users can integrate other Planning Center tools, such as event calendars, registration forms, and donation tracking. 

**\- Page Publishing Features:**

  **- Discard:** Test that users can undo changes made since their last save.

  **- Save Draft:** Ensure that users can save a draft of their page without publishing it.

  **- Save & Publish:** Test that users can publish their changes immediately.

  **- Page Navigation & Access:** Verify the functionality for copying the page URL, downloading the QR code, and setting access restrictions for specific membership types.

  **- View:** Confirm that users can successfully view their published page on Church Center.

**\- Page Visibility and Access Control:**

  **- Church Center Navigation:** Verify that pages added to the Church Center site navigation are visible to the intended users.

  **- Access Restrictions:** Ensure that pages with restricted access are visible but inaccessible to users without the appropriate membership type.

  **- Archiving and Removing Pages:** Test that users can archive pages or remove them from the navigation, effectively hiding them from public view.

**Non-Functional Testing**

**\- UI Smoothness and User Experience:** Test the responsiveness and ease of use across the application.

**\- Accessibility Testing:** Ensure compliance with accessibility standards (e.g., screen reader support, color contrast).

**\- Layout and Device Settings Modes and States:** Testing the UI under different conditions and layouts. (airplane mode, dark/light mode, system settings with different languages, landscape/portrait mode, split screen, low battery, throttled service)

**\- Cross-Browser and Mobile Device Testing:** Verify that the application functions consistently across various browsers and mobile devices.

**Performance Testing**

  **- Image Loading Performance**: Verify that images at least 700px wide load quickly on mobile devices without causing slowdowns. Assess loading times for images of varying widths to ensure optimal performance.

  **- Overall Performance:** Assess the application's performance under heavy loads, such as video streaming for sermons, ensuring stability, scalability, and quick response times.

**\- Usability Testing:**

  **\- Visual Quality on Mobile:** Evaluate whether images display correctly at full width on mobile devices and check if they maintain visual quality when scaled down on the web.

  **- User Experience:** Assess how users perceive images when viewed on different screen sizes. Check if images appear clear and enhance the overall content experience.

**\- Security Testing:** Ensure that restricted-access pages and features are properly secured, preventing unauthorized access.

**API Testing**

_API testing will verify the integration between the front end and back end, ensuring that all new features function as intended. This testing will focus on:_

**\- Endpoint Functionality:** Validate that all API endpoints work correctly and return the expected responses for various requests.

**\- Data Consistency:** Ensure that data submitted from the front end is correctly processed and stored in the back end.

**\- Error Handling:** Test how the API handles errors and ensures that meaningful error messages are returned for invalid requests.

**\- Performance:** Assess the API's response times under normal and peak load conditions, ensuring it meets performance standards.

**\- Security:** Verify that the API is secure, with proper authentication and authorization mechanisms in place to protect sensitive data.

API Docs Resource Guide ([https://developer.planning.center/docs/#/overview](https://developer.planning.center/docs/#/overview))

**End-to-End Testing**

_End-to-end testing will validate the entire user flow, from the creation of a custom page to its publication. This testing will confirm that all steps, from page design and content integration to publishing and access control, work smoothly together._

**\- End-to-End Tests:** Comprehensive end-to-end tests will be executed to ensure that the overall user experience remains intact and that all workflows function correctly after updates.

**Regression Testing**

_Regression testing will be conducted after significant code changes, the addition of new features, or before a release. The goal is to ensure that new developments do not adversely affect existing functionalities.  This will include:_

**\- Functional Automated Tests:** These tests will verify that all previously developed features continue to function as intended as new updates are pushed. This could include internal updates and features added by the dev team themselves as well as external third party updates to linked API’s, for example YouTube embedded videos and Map API data.

_The testing approach would be a combination of API, manual, automation, regression, integration, and beta testing. Starting with API testing to ensure endpoint validity and functionality, as well as data consistency and validation with the frontend and backend database. Moving onto manual and exploratory testing, charter testing, and session-based testing will be employed to establish possible test cases for each functionality, ensuring integration across various platforms and components while validating that all elements work together seamlessly in their respective environments._

_Once this testing is complete and presented for review by the development teams and QA leads, decisions can be made regarding which tests are necessary for automation and should be integrated into a CI/CD pipeline for regression testing. This will be complemented by traditional exploratory manual testing during new updates, allowing us to catch any new and obscure defects that automated tests might not identify. Finally, upon approval from product management, a beta version of the app will be released for users to test in real-world environments, providing user experience stories for the QA and development team to triage and address any issues before the final release._

3\. Test Environments

**Devices & Environments**

**\- Mobile Devices:** Testing will focus on the top 10 most used smartphone devices in the USA, targeting the application's performance and usability on these popular devices. 

**\- Desktop Operating Systems**: The tests will cover the top two operating systems for desktops: macOS and Windows, ensuring compatibility and a seamless user experience across platforms. 

**\- Web Browsers:** Testing will include the top 3 web browsers used in the USA to verify consistent functionality and design, including Chrome, Safari, and Firefox. 

**\- Tablets:** The top 5 tablets used in the USA will be incorporated into the testing process to ensure the application works effectively on larger screens. 

**\- Screen Resolutions:** Focus will be placed on the top 5 screen resolutions for desktops, ensuring that the UI adapts well across different display sizes. 

**Testing Tools**

**\- Android Studio and Chrome DevTools:** These tools will be used for layout and aspect ratio testing, allowing for device emulation to ensure the application displays correctly on various devices. 

**\- Postman:** Manual API testing will be conducted using Postman to validate API endpoints and ensure data consistency. 

**\- JavaScript/Jest/Mocha:** Automated API testing will be performed using these frameworks to streamline the testing process and ensure endpoint reliability. 

**\- UI Automation:** Testing will utilize frameworks such as Selenium or Playwright for UI automation, ensuring the application's interface functions correctly and provides a smooth user experience. 

4\. Team Communication and Version Control

**\- Bug reporting on Jira,** with prioritization focused on severity with status updates

**\- Daily or weekly stand-ups** to keep the team checked in

**\- Documentation** on a shared Google Drive or something similar

**\- GitHub** repo for version control and collaboration, and storage of automation code

5\. Examples of Key Testing Scenarios & Challenges

**Custom Page Creation:**

**1\. Creating a New Page:**

   - Test various title lengths

   - Input multiple languages (especially how it handles RTF languages)

   - Create pages without titles

   - Adding a link to a title

   - How do we handle conflicts when multiple admins are editing the same page simultaneously?

**2\. Adding Various Block Types:**

   - Drag and drop each different block types testing across various device types, functionality with mouse, trackpad, stylus, etc

   - Ensure layout consistency when combining block types

   - Test edge cases, like limiting pages to 12 blocks

**Block Types: (Key Testing Scenarios and Challenges)**

**Button block type: (Create a button and attach a hyperlink to it.)**

\- Functionality of the hyperlink attached to the button

\- Testing valid and invalid inputs for hyperlinks

\- Acceptance of different domain extensions

\- Limits on URL length and flexibility of abbreviated URLs

\- Correlation between the appearance of hyperlinks in unpublished drafts and published pages

**Contact block type: (Add contact information that congregants can select or tap to contact your church.)**

\- Acceptance of different phone number formats using various delimiters

\- Handling different country codes and phone number lengths

\- Managing invalid contact inputs

\- Proper redirection to the appropriate app (phone or email) for contact

\- Tap-to-contact functionality

\- Handling multiple contact blocks on the same page

**Event schedule block type: (Add a date, time, and description of an event.)**

\- Handling of past and future dates and times

\- Boundaries for description length

\- Inserting hyperlinks and emojis into event descriptions

\- Integration with scheduling blocks in the planning center ecosystem/database

\- Handling of invalid and valid dates

\- Display of local time zones and suggestion of current dates/times

\- Layout and aspect ratio on the published page

\- Managing multiple scheduling blocks

**Image block type: (Select an image from your device, your saved library, or the Unsplash integration. Attach a hyperlink to the image to use it as a button.)**

**(Please allow for extensive testing on this area of focus as it presents a large range of challenges.)** 

\- Testing image selection from the device, saved library, and Unsplash integration

\- Functionality across multiple devices when selecting images

\- Access to saved library: testing for maximum storage space, proper addition and deletion of files, and file types

\- Uploading large images: testing for speed and reliability

\- Edge cases for acceptable resolutions, as described in the image upload guide

\- Verifying different image types and sizes across multiple browsers and devices

\- Testing pages with multiple images near maximum file size and various resolutions

*   Error messages for invalid image sizes or types, ensuring they're user-friendly

\-Ensuring that images are resized or rejected if they do not meet the required dimensions

*   Testing Unsplash usability: does it display or suggest accurate images? Does it handle image sizing restrictions well?

\-Handling corrupted image files or interrupted uploads gracefully, ensuring the system does not crash or hang, and appropriate error messages are displayed.

\-Testing across different screen resolutions is necessary to avoid distortion or incomplete loading.

*   Testing hyperlinks attached to images: do they work as buttons? What types of websites are acceptable, loading times, and URL formats? Does adding a hyperlink alter the image's appearance?

\- **Requirement Resources** (https://support.planningcenteronline.com/hc/en-us/articles/18032518633115-Image-Sizing)

**Location block type: (Enter an address to generate a map view on the page.)**

\- Accurate display of various address formats

\- Integration with the map API (e.g., Google Maps)

\- Displaying different map views (satellite view, etc.)

\- Functionality of interacting with the map: zooming, changing directions, etc.

\- Resolution and aspect ratio of the map, ensuring readability

\- Handling of valid and invalid addresses

**Section header: (Add a header for a section of your page. You can add a background image, button, and text.)**

\- Testing valid and invalid file types and sizes for background images

\- Ensuring proper display across different environments, with appropriate cropping and aspect ratios

\- Functionality of adding buttons to headers

\- Limits on text length and display for headers

\- Managing multiple headers per page

**Social Block Type: (Add links to your church's social media pages, such as Facebook, Twitter, Instagram, TikTok, or YouTube.)**

\- Ensuring valid social media links are accepted

\- Testing what happens when invalid or broken links are added

\- Testing different link formats (e.g., shortened URLs)

\- Display and alignment of social media icons on different devices

\- Ensuring proper redirection to the correct platform when a link is clicked

\- Testing functionality across different browsers and devices

\- Handling multiple social media blocks and how they display when stacked

\- Testing how the social media links look in both draft and published versions

\- Verifying responsiveness of icons and links (do they resize appropriately on mobile vs. desktop?)

**Video Block Type: (Add a URL or embed code to a video hosted on YouTube, Vimeo, or Boxcast.)**

\- Acceptance of valid and invalid video URLs and embed codes

\- Functionality of video playback across different devices and browsers

\- Testing for video loading times and buffering issues

\- Verification of responsive design: does the video resize appropriately on mobile and desktop?

\- Handling of various video formats and qualities

\- Ensuring proper display of video controls (play, pause, volume, fullscreen, etc.)

\- Testing embedded videos for accessibility features, like captions and descriptions

\- Ensuring compatibility with different video hosting platforms (YouTube, Vimeo, Boxcast)

\- Error messages for invalid URLs or embed codes and their user-friendliness

**Grid Block Type: (Add multiple items, such as buttons and images with hyperlinks and texts, and display them in a grid with up to three columns. You can adjust the number of columns based on mobile and desktop views.)**

\- Acceptance of various item types within the grid (buttons, images, texts)

\- Testing layout and alignment of items across different screen sizes

\- Functionality of hyperlinks attached to buttons and images within the grid

\- Handling of different grid column configurations: testing with 1, 2, and 3 columns

\- Ensuring responsiveness: how does the grid adjust when switching between mobile and desktop views?

\- Validating that items maintain their proportions and visibility when resized

\- Testing for adequate spacing between items to prevent overlap

\- Handling of invalid or broken hyperlinks within grid items

\- Checking for accessibility features for buttons and images in the grid

\- Performance testing with a maximum number of items in the grid to ensure the page remains responsive and functional

\- Testing edge cases against the recommendation to not exceed 12 items per block.

**Planning Center Blocks - Key Testing Scenarios and Challenges**

_Maintaining data consistency between custom pages and other Planning Center products_

**Calendar Block Type: (Show up to six events, with past events dropping off automatically.)**

\- Test edge case limits for the number of events displayed

\- Ensure proper integration since this feature is imported from content generated in other areas of the Planning Center software

\- Verify that past events drop off in chronological order: how quickly are past events removed? What happens with repeating weekly events?

\- Check if the calendar is interactive: can users RSVP or click on events to be redirected for further details?

\- Test the display of canceled events to ensure they are marked or removed appropriately

**Giving Block Type: (Link to a specific fund.)**

\- Confirm that all funds can be added as a link

\- Ensure the link is functional and redirects to the correct fund page

\- Test proper integration since this feature is imported from content generated in other areas of the Planning Center software

**Publish a Page - Key Testing Scenarios and Challenges**

**Functionality of each page publishing option buttons:**

**1\. Discard Button**

\-Verify that all unsaved changes are undone and the page reverts to its last saved state. Is this dependent on acceptance of cookies, or device permissions? 

\-What is the behavior of this option during time of various internet connection strengths?

**2\. Save Draft Button**

\-Make sure all changes are saved without publishing. 

\-Test saving drafts with small alterations

\-Test saving drafts multiple times.

\-Retest discard button after saving a draft ensuring

**3\. Save & Publish Button**

\-Confirm that the page is published successfully and becomes viewable on Church Center.

\-Ensure the page is inaccessible in Church Center until you add it to the navigation. 

\-Ensure the publish version matches the draft and unpublished version.

*   Additional suite of testing scenarios can be developed using these requirements ([https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c](https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c))  
    

**4\. Page Navigation & Access Dropdown**

\-Test the QR code generated for the page to ensure it redirects to the correct published page, test the compatibility across various devices when scanning the QR code. 

\-Test the ability to copy the URL across various devices using several methods, such as keyboard commands, right click etc.

\-Ensure the URL itself is copied and is congruent with the expect URL

\-Observe the overall UI of the dropdown, ensure its functionality and display. What is the behavior of large list of blocks within the dropdown menu, are they properly ordered? 

**5\. User Access**

\-Test the functionality and security of different access limitations of published pages

\-Ensure the page titled is searchable and title is viewable even for those without access

\-Test pages that have zero access limitations and ensure they are fully accessible. 

\-Test accessibility to users who maybe limited to one or more pages.

\-Test accessibility for users logged in simultaneously on different devices.

\-Test minimum and maximum user access values when setting access limitations.

\-Explore possible bypasses to access limitation security such as users changing emails, phone numbers, other unique identifiers.   

\-Test the functionality of completely hiding the page from the public, explore pressure points such as rapidly toggling between hidden and viewable.

\-Explore the access capabilities of users who previously had permission to view non-public pages, specifically regarding their ability to see hidden or archived versions of these pages.

\-Additional suite of testing scenarios can be developed focusing on the functionality of archiving and removed published pages. 

([https://pcopublishing.zendesk.com/hc/en-us/articles/360051714154-Archive-or-Restore-a-Page#UUID-892df1b9-b1ff-cbd7-1fd4-357fca845e77](https://pcopublishing.zendesk.com/hc/en-us/articles/360051714154-Archive-or-Restore-a-Page#UUID-892df1b9-b1ff-cbd7-1fd4-357fca845e77)).

 ([https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c](https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c))

**Performance and Scalability Challenges**

\-Balancing performance with rich media content is crucial.

\-Ensuring quick loading times, especially for pages with multiple high-resolution images or videos.

\-Optimizing performance across various devices and network conditions without compromising quality.

\-Identifying performance bottlenecks that only appear under high load or with specific content combinations.

**Cross-Platform Consistency Challenges**

\-Maintaining a uniform experience across web and mobile platforms is demanding.

\-Ensuring responsive design works seamlessly on both desktop and mobile devices.

**Multi-language Support Challenges**

\-Ensuring the system works correctly for various languages and regions is complex.

\-Handling different date/time formats and time zones correctly, particularly for event-related features.

\-Implementing and testing support for right-to-left languages, especially in drag-and-drop interfaces.

6\. Prioritized Test Plan for Custom Pages Feature

**Sprint 1 Core Functionality and Critical Features (1-2 weeks)** 

**Page Creation and Basic Block Types** 

\-Create new pages with various titles and configurations -Test drag-and-drop functionality for all block types-Verify basic functionality of text, image, and button blocks -Test saving drafts and publishing pages 

**Critical Block Types and Integration** 

\-Test video block with various URLs and embed codes-Verify calendar block integration and event display-Test giving block functionality and fund linking-Ensure proper functioning of location block and map integration 

**User Access and Security** 

\-Test page access restrictions for different user types -Verify visibility settings (public, limited, hidden)-Test archiving and restoring pages 

**Sprint 2 Advanced Features, Performance, & Cross-platform Testing (1-2 weeks)** 

**Advanced Block Types and Layout** 

\-Test grid block with various configurations-Verify responsive design across different screen sizes -Test complex page layouts with multiple block types 

**Performance and Load Testing** 

\-Test page load times with various content combinations -Verify performance on slower network connections 

\-Test system behavior under simulated high user load 

**Cross-platform and Browser Testing** 

\-Test on top 3 mobile devices (iOS and Android) 

\-Verify functionality on top 3 desktop browsers (Chrome, Safari, Firefox) 

**Integration and Data Consistency** 

\-Verify data consistency between Custom Pages and other Planning Center products -Test simultaneous editing by multiple admins-Conduct end-to-end testing of user journeys (create, edit, publish, access) 

7\. Conclusion 

_The complexity of the software introduces various challenges, making it essential to divide testing into several focused areas. These areas should cover different components of the software, including database and API testing, web UI testing, and mobile UI testing. Achieving full test coverage across all combinations of content types, layouts, and user permissions can quickly become overwhelming. Therefore, finding the right balance is key. With so many device and browser combinations, exhaustive testing is unrealistic._

_To ensure testing is effective, we need to focus on the most critical challenges and scenarios—those that have the greatest impact on performance, functionality, and reliability, as described in the initial 2 sprints of this plan. Once these core areas are validated they can be transferred into automated tests for regression testing allowing manual testing to focus on deeper and more in-depth scenarios and challenges. The process can then repeat with each release based on user feedback and on-going future developments._ 

8\. Resource Links

Custom Page Overview ([https://pcopublishing.zendesk.com/hc/en-us/articles/360052458693-Create-a-Custom-Page#create-a-new-page-0](https://pcopublishing.zendesk.com/hc/en-us/articles/360052458693-Create-a-Custom-Page#create-a-new-page-0))

API Docs Resource Guide ([https://developer.planning.center/docs/#/overview](https://developer.planning.center/docs/#/overview))

Image Requirements([https://support.planningcenteronline.com/hc/en-us/articles/18032518633115-Image-Sizing](https://support.planningcenteronline.com/hc/en-us/articles/18032518633115-Image-Sizing))

Navigate Set-Up ([https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c](https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c)) 

Archive Page Set-Up ([https://pcopublishing.zendesk.com/hc/en-us/articles/360051714154-Archive-or-Restore-a-Page#UUID-892df1b9-b1ff-cbd7-1fd4-357fca845e77](https://pcopublishing.zendesk.com/hc/en-us/articles/360051714154-Archive-or-Restore-a-Page#UUID-892df1b9-b1ff-cbd7-1fd4-357fca845e77)).

Hide Page Set-Up ([https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c](https://pcopublishing.zendesk.com/hc/en-us/articles/360051692034-Navigation-Setup#UUID-fa895884-7a89-c5f7-bcd6-da7e36f0b81c))