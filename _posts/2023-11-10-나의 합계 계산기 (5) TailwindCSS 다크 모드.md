---
title: 나의 합계 계산기 (5) TailwindCSS 다크 모드
date: 2023-11-10 12:00:00 +09:00
categories: [my-sum-calculator]
tags: [web app, my-sum-calculator, tailwindcss, darkmode]
---

# Dark Mode

- <https://tailwindcss.com/docs/dark-mode>

## 📌 `tailwind.config.ts`{: .filepath}

```ts
{
  ...
   darkMode: "class",
  ...
}
```

## 📌 `src/components/Navbar.tsx`{: .filepath}

```ts
'use client';

import { useEffect } from 'react';

export default function Navbar() {
  useEffect(() => {
    const darkModeMediaQuery = window.matchMedia(
      '(prefers-color-scheme: dark)'
    );

    const toggleDarkMode = (
      e: MediaQueryListEvent | MediaQueryList | Event
    ) => {
      if ('matches' in e) {
        document.documentElement.classList.toggle('dark', e.matches);
      }
    };

    toggleDarkMode(darkModeMediaQuery);
    darkModeMediaQuery.addEventListener('change', toggleDarkMode);

    return () => {
      darkModeMediaQuery.removeEventListener('chagne', toggleDarkMode);
    };
  }, []);

  return (
    <div className='flex justify-between items-center h-[60px] px-4'>
      <nav>
        <ul className='font-bold'>나의 합계 계산기</ul>
      </nav>
      <nav>
        <ul>아바타</ul>
      </nav>
    </div>
  );
}
```

## 📌 `src/app/layout.tsx`{: .filepath}

```ts
import './globals.css';
import { Inter } from 'next/font/google';
import type { Metadata } from 'next';
import Navbar from '@/components/Navbar';

const inter = Inter({ subsets: ['latin'] });

export const metadata: Metadata = {
  title: '나의 합계 계산기',
  description: '수치의 합계를 보기 편하게'
};

export default function RootLayout({
  children
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang='en'>
      <body
        className={`${inter.className} bg-stone-100 dark:bg-stone-950 text-stone-950 dark:text-stone-100 `}
      >
        <header className='z-10'>
          <Navbar />
        </header>
        <main className='h-[calc(100vh-60px)]'>{children}</main>
      </body>
    </html>
  );
}
```
