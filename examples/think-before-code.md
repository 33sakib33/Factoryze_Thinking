# Think Before Code example

## Starting request

**User**

> Use `$think-before-code`. Make a clone of a popular task manager.

## Expected first response

**Agent**

> The named product is a reference, not a complete specification.
>
> 1. Who will use the first version, and what must that person complete?
> 2. Which parts of the reference must stay, change, or disappear?
> 3. What must the first version include and exclude?

The response does not list possible users, features, or clone boundaries. Those choices belong to the learner.

## Later technology gate

After the user defines behavior, limits, and module boundaries, the agent can ask:

> Which exact technology will each module use?
>
> State where it runs and why it fits a confirmed requirement.
>
> State one cost, risk, or limit introduced by each choice.

The agent can expose a conflict between the choice and the contract. It must not choose a replacement technology.

## Module readiness example

**User**

> The task-data module comes first because every other module reads its task records. It owns validation and storage. It does not own screen state.

**Agent**

> State the information this module accepts, returns, and rejects.
>
> State the rule that must remain true after every write.
>
> What exact checks must pass before this module is finished?

Implementation starts only after the project and first module meet the applicable readiness rules.
