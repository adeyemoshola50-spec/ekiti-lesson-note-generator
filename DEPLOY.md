# Deploy to Vercel (1 Minute)

1. Go to https://vercel.com/new
2. Import Git Repository -> select ekiti-lesson-note-generator
3. Framework: Vite (auto-detected) -> Build Command: npm run build -> Output: dist
4. Deploy
Your URL: https://ekiti-lesson-note-generator.vercel.app

Custom Domain:
Vercel -> Project -> Settings -> Domains -> Add ekitilessonnotes.com.ng -> Follow DNS instructions.

Env Vars (when you add backend):
Settings -> Environment Variables -> Add VITE_AI_API_URL
Redeploy.
