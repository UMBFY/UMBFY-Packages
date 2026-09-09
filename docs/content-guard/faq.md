# Content Guard FAQ

## Does Content Guard work with existing content?

Content Guard is designed to bootstrap/index supported existing references after installation so editors do not need to manually re-save every item.

## Does it respect Umbraco permissions?

Yes. Editor-visible details are authorization-aware; restricted dependencies can still influence safety decisions without exposing restricted information.

## Does it support every custom property editor?

No. Support is limited to documented editors/reference shapes unless a dedicated scanner is added.

## What happens while the index is rebuilding?

Content Guard should report an initializing/rebuilding state and avoid presenting incomplete data as fully safe or healthy.
