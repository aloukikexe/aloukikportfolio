<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## Project rules
- The portfolio is one full-screen scene canvas (`src/components/portfolio/Experience.tsx`) rendered at `/`; all scene changes go through `goTo()` so only one locked transition runs at a time.
- All copy, links and project data live in `src/data/portfolio.ts`; layout code reads from it so content edits never touch components.
- Elements animated with GSAP transforms must not also carry Tailwind `translate-*` classes: GSAP folds the CSS `translate` property into its own offset and the element ends up displaced (this parked the scene curtain over the screen).
