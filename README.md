# Why (justification, context)

1. Is it clear what problem the change solves?
* Is it stated in the commit title?
* Is there a relevant ticket linked in the commit message?

2. Are we sure it's worth to make this change?
* Will solving this problem pay off?
* Is the cost of solving it lower than the the cost of living with the exisitng issue?

# What (functional aspects)

1. Is the proposed solution the right way to solve this issue, assuming it works as intended?
* Is the proposed user experience approved or designed by someone entitled to do it?
* Is it clear or explicitly stated if the solution is short-, mid- or long-term?

2. Does the happy/common path work correctly?
* Has it been tested end-to-end that a common scenario works?
* Is testing methodology described or obvious?

3. Are edge cases covered?
* How can we be sure all (relevant) edge cases are identified?
* Are they handled correctly?

4. Is the feature ready to be exposed to the public?
* Should there be grace period before this change is made, if it's a breaking one?
* Should the feature be hidden behind a feature flag?

5. Are there any prerequisites or dependencies that must be fulfilled before this change is made?
* Are all dependencies aware of extra traffic?
* Are relevant permissions granted on all environments and stages, from all dependencies?

6. Is there anything extra needed for the customer?
* Is documentation in place?
* Does the customer know how to report issues with this change?

# How (architectural aspects)

(Raw notes, TODO: clean up)
* does this change reinvent the wheel (reimplement something)? Can some code be taken from a
  generic place, to maintain consistency with how it works in other places? Example: there was
  filtering in some part of the system, custom-made, but only partially. It used some library
  functions, but some things were done in a custom way. It led to a bug

1. Are troubleshooting facilitators in place?
* Is there proper logging?
* Are relevant IDs (request IDs, order IDs) exposed to the customer wherever needed?
* Is any sensitive data logged?

2. Is the change structured properly?
* Are there any unrelated changes (formatting changes, fixing something "while being there")
* Are commits small enough to be understood easily?
* Are there any refactorings that could be separate commits?

3. In case of bugs, are there regression detection mechanisms in place?
* Is there a test that would break before fixing the issue?
* Are the tests good enough to detect accidental changes in code (mutation testing)?

4. Is the code clean?
* Does it read like an article (from general description, down to details)?
* Does it contain logic that is easy to understand, or is it documented otherwise?

5. Is performance optimal or at least known?
* Has the change been tested for bigger amount of data?
* How does it scale in terms of data growth?
