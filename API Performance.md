# Strategies I hadn't thought of
1. Reduce polling with event-driven, asynchronous, or pub-sub APIs
2. Use connection pools
3. compress payloads
4. Use asynchronous logging:
> Synchronous logging means your system calls the system log _for every interaction_, which is horribly inefficient. Putting an asynchronous logging system in place is an easy way to prevent that from happening. An asynchronous logging system sends a log to a lock-free buffer, where they are stored before being sent to the registry periodically.
> 
> Having an asynchronous logging system in place improves API performance in numerous ways. Asynchronous loggers can log messages [six to 68 times faster](https://logging.apache.org/log4j/log4j-2.3.2/manual/async.html) faster than a synchronous log, according to Apache. They also reduce latency, as the log doesn’t need to be called for every interaction. Latency spikes are kept to a minimum, helping to ensure smooth performance even during traffic spikes.

