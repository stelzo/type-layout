> [!NOTE]  
> This is only a patched version of the original [type-layout](https://crates.io/crates/type-layout) for using syn 2 instead of syn 1. This crate will be yanked when the original author applied the patch. See the [PR](https://github.com/LPGhatguy/type-layout/pull/9) for progress on this matter.
> The patch contains following changes:
>
> - Use syn v2 as dependency instead of syn v1.0.40.
> - Use memoffset v0.9 instead of v0.5 for fixing a known bug in memoffset where uninitialized memory could be read.
> - Update Rust MSRV to 1.60 (inherited from syn 2).
> - Change Field struct to enum in TypeLayoutInfo from published source to be feature-synced with v0.2.0 on crates.io.
>
> Use this patch like this `type-layout = { version = "0.2", package = "type-layout-syn2" }`.
> While the changes are technically breaking, the original author will decide the actual version.
