## Started Project

### Documentation

https://ui.shadcn.com/docs/installation/next

```
% npx create-next-app@latest ecommerce-admin --typescript --tailwind --eslint

Need to install the following packages:
  create-next-app@13.4.9
Ok to proceed? (y) y
✔ Would you like to use `src/` directory? … No / Yes N
✔ Would you like to use App Router? (recommended) … No / Yes Y
✔ Would you like to customize the default import alias? … No / Yes N
```

UIライブラリにshadcnを使用

```
% npx shadcn-ui@latest init

Need to install the following packages:
  shadcn-ui@0.3.0
Ok to proceed? (y) y
✔ Would you like to use TypeScript (recommended)? … no / yes y
✔ Which style would you like to use? › Default
✔ Which color would you like to use as base color? › Slate
✔ Where is your global CSS file? … app/globals.css
✔ Would you like to use CSS variables for colors? … no / yes y
✔ Where is your tailwind.config.js located? … tailwind.config.js
✔ Configure the import alias for components: … @/components
✔ Configure the import alias for utils: … @/lib/utils
✔ Are you using React Server Components? … no / yes y
✔ Write configuration to components.json. Proceed? … yes
```

### Componentごとのインストール

dialogの場合

`npx shadcn-ui@latest add dialog`

これを実行すると、components/ui配下にdialog componentが作られる


### App Router ディレクトリ構成

https://nextjs.org/docs/app/building-your-application/routing/route-groups


## 認証

clerk

登録してプロジェクト作成

https://clerk.com/?utm_source=www.google.com&utm_medium=referral&utm_campaign=none

Doc

https://clerk.com/docs/nextjs/get-started-with-nextjs


`npm install @clerk/nextjs`


### 状態管理

`npm install zustand`


### Form

shadcnのformとinputを使用する。このformにreact-hook-form、zodが含まれている。

https://ui.shadcn.com/docs/components/form

https://ui.shadcn.com/docs/components/input
