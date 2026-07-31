# Setup & Deployment Instructions

## Prerequisites
- Node.js 18+ installed
- npm, yarn, or pnpm package manager

## Getting Started Locally

### 1. Install Dependencies
```bash
pnpm install
# or: npm install / yarn install
```

### 2. Run Development Server
```bash
pnpm dev
# or: npm run dev / yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the website.

### 3. Make Your Customizations
- Edit `components/ui/RelationshipTimer.tsx` - Update relationship start date
- Edit `components/sections/LoveLetter.tsx` - Your love letter
- Edit `components/sections/ReasonsILoveYou.tsx` - Reasons you love them
- Edit `components/sections/Timeline.tsx` - Your timeline milestones
- Edit `components/sections/RomanticQuotes.tsx` - Your favorite quotes
- Add images to `public/assets/gallery/` and update PhotoGallery.tsx
- See `CUSTOMIZATION_GUIDE.md` for complete details

### 4. Preview Your Changes
The dev server has hot reload - just save and the website updates automatically!

## Building for Production

```bash
pnpm build
pnpm start
```

## Deployment Options

### Option 1: Deploy to Vercel (Recommended)
Vercel is the creators of Next.js and provides the best experience.

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin YOUR_REPO_URL
   git push -u origin main
   ```

2. **Connect to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Click "Deploy"
   - Your site is live! 🎉

3. **Custom Domain**
   - In Vercel dashboard, go to Settings > Domains
   - Add your custom domain
   - Follow DNS configuration steps

### Option 2: Deploy to Netlify

1. **Push to GitHub** (same as above)

2. **Connect to Netlify**
   - Go to [netlify.com](https://netlify.com)
   - Click "New site from Git"
   - Select your repository
   - Build command: `pnpm build`
   - Publish directory: `.next`
   - Click "Deploy site"

### Option 3: Self-Hosted

1. **Build the project**
   ```bash
   pnpm build
   ```

2. **Copy to your server**
   - Copy the `.next` folder
   - Copy `node_modules` folder (or run `pnpm install` on server)
   - Copy `package.json`
   - Copy `public` folder

3. **Start on server**
   ```bash
   NODE_ENV=production pnpm start
   ```

## Project Structure

```
├── app/
│   ├── layout.tsx           # Root layout with fonts
│   ├── page.tsx             # Main page
│   └── globals.css          # Global styles & animations
├── components/
│   ├── animations/          # Confetti, scroll progress, etc.
│   ├── sections/            # Page sections (Hero, Gallery, etc.)
│   └── ui/                  # Reusable UI components
├── lib/
│   └── config.ts           # Centralized configuration
├── public/
│   └── assets/             # Images, videos, media
├── CUSTOMIZATION_GUIDE.md  # How to customize everything
└── package.json            # Dependencies
```

## Environment Variables

This project doesn't require environment variables for basic usage. All configuration is in:
- Component files
- `lib/config.ts`
- `app/globals.css`

## Troubleshooting

### Port 3000 already in use
```bash
# Use a different port
pnpm dev -p 3001
```

### Dependencies installation issues
```bash
# Clear cache and reinstall
rm -rf node_modules pnpm-lock.yaml
pnpm install
```

### Images not loading
- Ensure images are in `public/` directory
- Check paths in component files
- Use relative paths: `/assets/gallery/image.jpg`

### Animations not working
```bash
# Restart dev server
# Then check browser console for errors
```

## Performance Optimization

1. **Image Optimization**
   - Compress images before adding
   - Use Next.js Image component (already done)
   - Recommended size: 500x500px for gallery

2. **Video Optimization**
   - Use H.264 codec
   - Recommended bitrate: 1-2 Mbps
   - Format: MP4

3. **Font Optimization**
   - Using optimized Google Fonts
   - CSS minified automatically

## Browser Support

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Mobile browsers: ✅ Full responsive support

## Performance Metrics

The site targets:
- Largest Contentful Paint (LCP): < 2.5s
- First Input Delay (FID): < 100ms
- Cumulative Layout Shift (CLS): < 0.1

## Maintenance

### Regular Updates
```bash
# Check for updates
pnpm outdated

# Update packages
pnpm update
```

### Adding New Features
Follow the component pattern in `components/` to add new sections.

## Need Help?

- Check `CUSTOMIZATION_GUIDE.md` for content changes
- Visit [Next.js Docs](https://nextjs.org/docs)
- Check [Framer Motion Docs](https://www.framer.com/motion/)
- Review [Tailwind CSS Docs](https://tailwindcss.com)

## License

This project is created for personal use. Feel free to modify and share with your loved one! 💕

---

**Happy sharing! May your website capture the essence of your beautiful love story.** ❤️
