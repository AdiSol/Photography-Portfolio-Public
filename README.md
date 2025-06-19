# Video & Photography Portfolio Website
A modern, responsive portfolio website built for a creative professional to showcase their photo and video editing work. This was built for Jeremiah Manzano. This is for public viewing and not the finalized version the client will be using.

## Live Demo
**Deployed on Vercel:** https://www.jeremiahmanzano.com/

## Mockup
* First created a mockup for the client based on their design inspiration and specfication to consolidate the plan for the portfolio website.
* https://www.figma.com/proto/dhTd2oMVyUKLgAWpriSgpX/Capule-Studios?node-id=27-56&t=xezS8ATproJIz2SQ-1

## 🛠️ Tech Stack
* Framework: Next.js 14
* Language: TypeScript
* Deployment: Vercel
* Forms: Web3Forms
* Video Hosting: YouTube (embedded)
* Styling: Modules

## 📸 Screenshots
![image](https://github.com/user-attachments/assets/85c71e16-ae5e-4d71-97de-7b725ed1c5c0)
![image](https://github.com/user-attachments/assets/66ca9859-e7a0-4f1f-8581-0c704c8e543a)
![image](https://github.com/user-attachments/assets/05b6d006-b0bc-4d86-9679-aacf1fd5fe1b)
![image](https://github.com/user-attachments/assets/30b96c9a-b7b0-4b8b-9bf8-442fb57fb0bb)

## ✨ Features
### Core Functionality

* **Home Page**: Clean, professional landing page introducing the client's work

* **Photo Gallery**: Interactive before/after comparison using image sliders to showcase photo editing skills
* **Video Showcase**: Curated collection of video editing projects and reels
* **Contact Form**: Functional contact system using Web3Forms for reliable message delivery
* **Content Management**: File-based CMS for easy image management and updates
* **Image Protection**: Multiple layers of protection to safeguard client's creative work

### Technical Highlights

* **Performance Optimized**: Implemented lazy loading and Next.js image optimization for fast load times
* **Cost-Effectiv**e: Strategic use of YouTube embeds to minimize hosting costs and bandwidth usage
* **Responsive Design**: Fully responsive across all device sizes
* **Modern Stack**: Built with Next.js 14 and TypeScript for type safety and developer experience

## 🚀 Key Technical Decisions
### Performance & Optimization

* **Image Optimization**: Leveraged Next.js built-in image optimization for automatic format selection (WebP, AVIF) and responsive sizing
* **Lazy Loading**: Implemented intersection observer-based lazy loading to improve initial page load speeds
* **Code Splitting**: Automatic route-based code splitting via Next.js for optimal bundle sizes

### Cost & Infrastructure Considerations

* **YouTube Integration**: Chose YouTube embeds over direct video hosting to minimize storage costs and leverage YouTube's CDN for optimal video delivery
* **Serverless Deployment**: Utilized Vercel's edge network for global performance without server maintenance overhead
* **Third-party Forms**: Integrated Web3Forms to avoid backend complexity while maintaining reliable form functionality
* **File-based CMS**: Implemented content management without database overhead, reducing infrastructure complexity and costs

### Content Management & Security

* **File-based CMS**: Streamlined content updates through file system management, allowing easy addition and organization of portfolio images
* **Image Protection Suite**:

* Disabled right-click context menus to prevent easy image saving
* Transparent overlay implementation that obscures direct image access
* CSS-based protection against common download methods


* **Intellectual Property Considerations**: Balanced user experience with creative work protection for professional portfolio use

### User Experience

* **Interactive Photo Comparisons**: Custom before/after slider components for engaging photo editing demonstrations
* **Smooth Navigation**: Optimized routing and prefetching for seamless user experience
* **Accessibility**: Semantic HTML and proper ARIA labels for screen reader compatibility
