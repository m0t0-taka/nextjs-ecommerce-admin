## Started Project

```
npm run dev
```

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

UI ライブラリに shadcn を使用

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

### Component ごとのインストール

dialog の場合

`npx shadcn-ui@latest add dialog`

これを実行すると、components/ui 配下に dialog component が作られる

### App Router ディレクトリ構成

https://nextjs.org/docs/app/building-your-application/routing/route-groups

## 認証

clerk

登録してプロジェクト作成

https://clerk.com/?utm_source=www.google.com&utm_medium=referral&utm_campaign=none

Doc

https://clerk.com/docs/nextjs/get-started-with-nextjs

`npm install @clerk/nextjs`

## 状態管理

`npm install zustand`

## Form

shadcn の form と input を使用する。この form に react-hook-form、zod が含まれている。

https://ui.shadcn.com/docs/components/form

https://ui.shadcn.com/docs/components/input

## Prisma

ORM として Prisma を使用する。

https://www.prisma.io/

```
npm i -D prisma
npm install @prisma/client
npx prisma init
```

これにより.env に環境変数がセットされる

## DB

DB は MySQL を使用する。

MySQL の使用は PlanetScale を利用する。

https://planetscale.com/

schema.prisma に schema 定義後は、

```
npx prisma generate
npx prisma db push
```

参考：https://planetscale.com/docs/prisma/prisma-quickstart#initialize-prisma

次のようなエラーが出る場合、DB（planetscale）が止まっている（sleeping になっている）ので起こしてあげる必要がある。

```
Unhandled Runtime Error
Error:
Invalid `prisma.store.findFirst()` invocation:

Error querying the database: Server error: `ERROR HY000 (1105): unavailable: unable to connect to branch
```

### DB のリセット方法

```
npx prisma migrate reset
npx prisma generate
npx prisma db push
```

## HTTP リクエストの扱い

axios を使用する。

## react-hot-toast

`npm i react-hot-toast`

## Cloudinary

https://cloudinary.com/

Next.js 用の Documentation

https://next.cloudinary.dev/

```
npm install next-cloudinary
```

## レアな Tailwind CSS 控え

- transition-colors
  色の変更を滑らかにする

- shrink-0
  これにより、flexbox でも、自動的に縮小されるのを防ぐ

## 学習メモ

#### TypeScript の extends

型定義を継承するときは extends を使用する。

#### lucide-react

icon のライブラリ。shadcn install 時に一緒にされる。
