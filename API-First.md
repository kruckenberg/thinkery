# Amazon API Mandate
>1. All teams will henceforth expose their data and functionality through service interfaces.
>2. Teams must communicate with each other through these interfaces.
>3. There will be no other form of interprocess communication allowed: no direct linking, no direct reads of another team’s data store, no shared-memory model, no back-doors whatsoever. The only communication allowed is via service interface calls over the network.
>4. It doesn’t matter what technology they use. HTTP, Corba, Pubsub, custom protocols — doesn’t matter.
>5. All service interfaces, without exception, must be designed from the ground up to be externalizable. That is to say, the team must plan and design to be able to expose the interface to developers in the outside world. No exceptions.
>6. Anyone who doesn’t do this will be fired.
>7. Thank you; have a nice day!

[Source](https://nordicapis.com/the-bezos-api-mandate-amazons-manifesto-for-externalization/)

# Conway's Law
It'd be fair to say that our APIs reflect our organization. That's not a good thing.

# Hyrum's Law
One reason that API design matters. We have to make smart decisions about what to expose, what we're willing to support, and how to wean users from functionality that we are no longer willing to support.

>With a sufficient number of users of an API, it does not matter what you promise in the contract: all observable behaviors of your system will be depended on by somebody.

