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
