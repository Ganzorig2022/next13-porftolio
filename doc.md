### Import alias

```json
{
  "compilerOptions": {
    "target": "es5",
    "lib": ["dom", "dom.iterable", "esnext"],
    "allowJs": true,
    "skipLibCheck": true,
    "strict": true,
    "forceConsistentCasingInFileNames": true,
    "noEmit": true,
    "esModuleInterop": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "preserve",
    "incremental": true,
    "plugins": [
      {
        "name": "next"
      }
    ],
    "paths": {
      "@/*": ["./*"]
    }
  },
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx", ".next/types/**/*.ts"],
  "exclude": ["node_modules"]
}
```

### React Fragment with map.key

```js
<div>
  {projectsData.map((project, index) => (
    <React.Fragment key={index}>
      <Project {...project} />
    </React.Fragment>
  ))}
</div>
```

### Hash to jump another section in page

> #projects heseg rvv userhed id="projects"

```js
//

<Link
  href="#projects">
</Link>

<section
  ref={ref}
  id='projects'
  className='scroll-mt-28 mb-28'
>
  <SectionHeading>My projects</SectionHeading>
  <div>
    {projectsData.map((project, index) => (
      <React.Fragment key={index}>
        <Project {...project} />
      </React.Fragment>
    ))}
  </div>
</section>
```

### Intersection Observer API

> React implementation of the Intersection Observer API to tell you when an element enters or leaves the viewport.
> https://www.npmjs.com/package/react-intersection-observer
