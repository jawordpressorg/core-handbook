# Preparing the About Page

Every WordPress release has an About page. It is shown to users after they finish updating to the new version and includes what the new features are and who contributed to making them.

This is a great marketing opportunity as lots of people get to see this page. It would be fun to have each major About page customized by one of the designers in the WordPress community (otherwise, we fall back on an existing design).

This trend started with WordPress 4.7, you can view the previous designs on Figma: [https://www.figma.com/file/LrjiQZDts99EakxvZ6YcuMIr/About-Page](https://www.figma.com/file/LrjiQZDts99EakxvZ6YcuMIr/About-Page)

If you want to create a page like this, here are the steps to follow:

## Steps

*   **Know your deadline**: Work on the About page starts once the release reaches Beta 1 and should be complete by RC1.
*   Create a ticket for the About page kick-off, like this: [https://core.trac.wordpress.org/ticket/46901](https://core.trac.wordpress.org/ticket/46901)
*   Clearly state what steps are:
    *   Coordinate between release leads and either marketing or a copywriter to draft initial page copy
        *   Draft in a google doc so multiple people can write and suggest edits
        *   Check-in with release leads about headline features
        *   Check-in with any feature leads if you’re unclear about details
        *   Go through Beta posts on /news/ to populate features and find copy inspiration
        *   Go through dev notes on make/core to populate developer happiness section
        *   Make sure to go through the features of Gutenberg and create a section to call it out with “new editor feature this release.”
    *   Create images — could be illustrations, icons, or screenshots
    *   Finalize copy (after release lead last review)
    *   Finalize design
    *   Get the page made up
    *   Test the page in various browsers, checking for image quality
*   Release Post (for those leading a release)
    *   Draft new post on wordpress.org/news
    *   Copy content over from the About page
    *   Add images, changing size, alignment, or positioning to fit the blog layout
    *   Pass off to release lead to include credits shortcode and release name
    *   Get the musician’s name from the release squad lead.
    *   Post slug should be wp.org/news/yyyy/mm/musician.
    *   Keep the post with an “album cover” feel.

## Copy

*   **Audience**: WordPress users and practitioners who are not active in contributing. Assume non-technical.
*   **Purpose**: To highlight the immediately interesting things and inspire people to experiment and/or learn more. Assume no need to sell WordPress to them.
*   **Property**: WordPress software
*   **Assets**: Assume that the copy flow will follow the design flow.
*   **Voice**: Aim for the positive side of neutral, though you can go all the way to cheerfully American Southern. Not a sales-y voice, since these are people already using WordPress.

## Design 

The About Page has a set framework and it is not meant to be redesigned from scratch each release.

The layout should be considered a stack of containers, which can be 1-4 columns. The content in the columns can be anything — text, video, images, embeds, etc. These containers can have no background color, a “subtle” background color, or “accent” background color (these change with each About page using colors from the header feature). Columns can also have one of these background colors. Containers are stacked on top of each other to create the page.

Wondering why the About Page is not done in the block editor? The biggest blocker is translations. Every string on the page is wrapped in a translation function, with additional translation notes as needed. We’d need to find a way to do that with Gutenberg as well. 

Some items to watch for:

*   The header has the most freedom. It can have a design element background or text effect. Check that it is accessible.
*   Images, illustrations, and videos are allowed in the content.
*   There can be 1, 2, 3, or 4 columns and have a colored background.
*   For tech requirements, look here: [https://gist.github.com/ryelle/91ef6cd84a197b6af880dc055be21cc9](https://gist.github.com/ryelle/91ef6cd84a197b6af880dc055be21cc9)
*   Talk to @ryelle about it. She is in charge of coding and committing the About Page.

Examples of how the boxes can look like:

![](https://lh5.googleusercontent.com/DVRYyXvASA9mholS4C8zhTT21GDAjmoTg0UeKn9tqOXIJVfL17eIryA-cqjV6bKKcUzdtUZ2hH6lTj4oalUSipk1DTxYiSUNCWnGbQOFgXsZsAGFpzTrYpr-a-BF5NNvTXEVqMgL)

![](https://lh3.googleusercontent.com/I58udBWS-OY14yd79gM87tkAq7Jd2efaLEA2E4FBh8487nqEckIs6FJ7CPzPDZR0XRbgarYYgoVvM3abLkH0k671ZaJXgUwvoyE5crrIwPjOg0g056OSvoOM8PWuRG0RKtX9_TtT)

![](https://lh5.googleusercontent.com/sccyLw1NoSYkxnpj-CchUCP9SBMAC6CgERLSYB4An8PHNHWaFFchrtrrXHTX4Vui3fS3FPldiQ8zZFsPg5GUfvMP46NJtoOk24M2ighkCzkI1MDPXyiw5mDkQIPvd8ssT4aqly-E)

### Images and Videos

There are requirements for images and videos.

### Images

For better understanding see the image below, some things to consider:

*   Images can be edge-to-edge or have a 32px padding on all four sides.
*   We don’t recommend putting images or videos in 3 & 4-column containers.
*   Images and videos resize a bit on mobile.

![](https://lh3.googleusercontent.com/fmu4dB-jRJYzIQaAE-7VNLzfc-F_4MXgpXomSr2itpDNoI4sQXAPSbXRt5_iJ-Q5oVTRKSHU-VanFvDNi4Nx1HGG_AYSJGbCkHLdsUmVbA72kCuqZJax70kaVzSUuwUUzjropi6v)

### Videos

**For accessibility,** if the video has voice audio, a text equivalent needs to be provided. If the video shows a flow or action being performed, then the process needs to be described in the text. The key thing is remembering the target audience for the description and that they need to get the same level of information from the description as a sighted audience gets from watching.

What matters is that it’s clear that the video’s description is associated with the video. figure/figcaption would probably suffice there. The figcaption should be connected to the figure using aria-labelledby; this is required to support IE11.

**Tech reqs**

*   Videos must be 480 px wide  (in general, most users will see this video at 436px wide, large phone sizes might see it up to 488px)
*   The space for a full-width video is 936px wide, and for a wider 2 column layout is 602px.
*   Record using Kap (this is different than the recommendation in the post but [@joen](https://profiles.wordpress.org/joen) recommended this instead of Screeny)
*   Convert .mov files to .mp4 using FFMPEG. Kap does appear to have the ability to export as MP4 and WebM though. Using that is preferable to converting if it works well.
*   [How to: Good UI demo videos](https://automattic.design/2019/11/12/good-ui-demo-videos/)

## Props

The props (or credits) within a release are collected by the Release Squad, and embedded in the About Page (and Release Announcement Post) via a shortcode. Gutenberg credits are collected via GitHub and added to the Credits API via a Meta Trac ticket (e.g., [5.7](https://meta.trac.wordpress.org/ticket/5649)). All non-code contributions are gathered by the Release Squad focus leads and also added to the Credits API. Finally the list of Noteworthy Contributors is assembled by the Release Squad and submitted as a Credits API update (e.g., [5.7](https://docs.google.com/spreadsheets/d/11pA2LM67fQ3q89ok-oMcGlzE1_vOJkPBMkn1tLGtWbI/edit#gid=1989970429)).

When working to match GitHub usernames to WordPress.org usernames you can use [`https://profiles.wordpress.org/github:username`](https://profiles.wordpress.org/github:noisysocks) where putting the GitHub username at the end of that URL will translate to the respective WordPress.org profile. This will work for any user who has [associated their GitHub account with their WordPress.org profile](https://make.wordpress.org/core/2020/03/19/associating-github-accounts-with-wordpress-org-profiles/). There is a similar method for converting a Slack username to a WordPress.org username by using [`https://profiles.wordpress.org/$slack_id`](https://profiles.wordpress.org/%24slack_id) where the Slack ID comes from a Slack user’s details (Click and avatar > View full profile > More \[…\] > Copy ID).