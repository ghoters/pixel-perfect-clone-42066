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

- Preserve the source project's three TanStack routes, shared components, CSS tokens and original image assets for visual parity; do not redesign the interface during migration.
- Keep downloaded source-project media as newly uploaded local project asset pointers; source-project pointers are scoped to their original project.
- Keep the reference-image redesign scoped to the order route and its `.order-page` styles so the other two source-faithful pages stay unchanged.
