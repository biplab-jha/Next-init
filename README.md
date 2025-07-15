# Next-init

Initialising the Next-JS, including Tailwind, PostCSS, & Autoprefixer and Shad-CN UI

After Installing NextApp,

`npm install -D tailwindcss postcss autoprefixer`

`npx tailwindcss@3 init -p`


**Tailwind.config.mjs**

```/** @type {import('tailwindcss').Config} */

export default {

  content: [
  
    './pages/**/*.{js,ts,jsx,tsx,mdx}',
    
    './components/**/*.{js,ts,jsx,tsx,mdx}',
    
    './app/**/*.{js,ts,jsx,tsx,mdx}',
    
    './src/**/*.{js,ts,jsx,tsx,mdx}',
    
    './node_modules/@shadcn/ui/**/*.{js,ts,jsx,tsx}'
    
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

**Global CSS:**

`@tailwind base;`

`@tailwind components;`

`@tailwind utilities;`


**ShadCN-UI:**

`npx shadcn@latest init`

`npx shadcn-ui@latest add button`

`npm install class-variance-authority tailwind-variants lucide-react`


**To Test:(page.js)**

```import { Button } from "@/components/ui/button";

export default function Home() {
  return (
    <main>
      <Button>Click Me</Button>
    </main>
  );
}
```

**Next.config.mjs**

```/** @type {import('next').NextConfig} */
const nextConfig = {
  reactStrictMode: true,
  experimental: {
    serverActions: true
  }
};

export default nextConfig;
```

**PostCSS.config.js:**
```
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```


