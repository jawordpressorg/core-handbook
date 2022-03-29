# Code Refactoring

Code refactoring should not be done just because we can. There are a number of “refactoring” tickets that have been opened over time, such as suggestions to rename long-standing functions or conform to more-recently established coding standards. Meanwhile, plenty of tasks are far more worthy of effort. Here are some suggested guidelines on what these tickets need in order to warrant review:

*   **Unit tests**, even if the code was not previously covered. We can’t afford regressions, and this will improve our test coverage.
*   **Performance benchmarks**, before and after. We can’t afford regressions.
*   **Proper justification and clear rationale** of changes are both necessary. Too often it is impossible to determine the purpose, objective, or focus of these patches. Code should not be rewritten under the cloaks of readability, narrow personal opinion, or general subjectiveness.

When none of this is followed, the end result is that reviewers and committers are distracted, which drains important attention and focus that should be spent elsewhere.

In addition, code refactoring can cause existing, more important patches to unnecessarily become stale.

There’s a document on contributing to the Linux kernel with [a section on pitfalls](https://dri.freedesktop.org/docs/drm/development-process/4.Coding.html#coding-style) when handling coding standards. I believe this can apply to the wider picture of refactoring as well (emphasis added):

> The kernel has long had a standard coding style, described in Documentation/CodingStyle. For much of that time, the policies described in that file were taken as being, at most, advisory. As a result, there is a substantial amount of code in the kernel which does not meet the coding style guidelines. The presence of that code leads to two independent hazards for kernel developers.
> 
> **The first of these is to believe that the kernel coding standards do not matter and are not enforced. … The other trap is to assume that code which is already in the kernel is urgently in need of coding style fixes.**

That said, we want to be internally consistent and follow our own rules. Code is poetry, and our code should be beautiful.