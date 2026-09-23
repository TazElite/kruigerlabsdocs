---
title: "FiveM Installation FAQ"
description: "Common FiveM installation, folder, ensure, dependency and restart questions."
category: "FAQ"
order: 500
keywords: "FiveM Installation FAQ frequently asked questions"
---

# FiveM Installation FAQ
<details><summary><strong>Where exactly does a resource go?</strong></summary><p>Put the complete resource folder under <code>resources</code> or a bracket category. The resource's <code>fxmanifest.lua</code> should be directly inside that resource folder.</p></details>
<details><summary><strong>Can I rename a resource?</strong></summary><p>Only when its documentation says that is supported. Exports, dependencies and code can refer to the original resource name.</p></details>
<details><summary><strong>Why does it work after I manually restart it?</strong></summary><p>That commonly points to start order or a dependency that was not ready during the cold boot.</p></details>
<details><summary><strong>Should I ensure every resource separately?</strong></summary><p>You can ensure individual resources or bracket categories. Explicit lines are easier to reason about when start order matters.</p></details>
<details><summary><strong>Why is FiveM saying the manifest is missing?</strong></summary><p>Check for an extra nested folder and confirm <code>fxmanifest.lua</code> is inside the actual resource directory.</p></details>
