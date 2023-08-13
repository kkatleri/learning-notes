# Kansas City - Java User Group - Meetup
    Location - Garmin HQ, Olathe, KS
    Date - 08/10/2023
    Organizer - Bill Kornado
    Speakers
        - Pratik Patel (Azul Systems) - Java for Serverless cloud functions

# Updates
- Java 21 release coming up with LTS (Long term support)

# Java for Serverless cloud functions
- Serverless is just not applicable to cloud functions but whole other bunch of cloud services.
- e.g You may be wanting to have database that is functional 1 hour in the morning and then do not require it.
- Problems with Serverless cloud funtions using Java
    - Startup 
    - Memory footprint
- Lambda platform itself takes 3 secs to start - standard
- On top, other startup time includes
    - JVM startup
    - JIT startup
        - JIT takes 20-30 mins to reach peak optimization and efficiency
    - Garbage collection
- Tips for Java Serverless cloud functions
    - Tip 1: KISS (Keep it simple stupid)
        - Small
        - Single purpose
        - Short running
        - Stateless
            - Generally in serverless architecture, state is offloaded externally, mostly on Redis
    - Tip 2: Build an Even Driven Architecture
        - SYNC
        - ASYNC
        - Events can be almost anything
    - Tip 3: Loose coupling and high cohesion
    - Tip 4: Use modern java
    - Tip 5: Be practical

- GraalVM
    - Benefits: AOT (Ahead of Time) compilation
    - Drawbacks: 
        - Reflection does not work at runtime
        - Peformance degrades in the long run
    - Generally not recommended to use for Serverless cloud functions

- CRaC (Coordinated Restore at Checkpoint)
    - Helps take the snapshot/image of the java instance
    - Generally good to take this snapshot immdiatedly after app startup and ready to serve the request
    - That snapshot can be used later to start the java instance again
    - Tremendously helpful for Serverless java cloud functions to reduce warm-up and start-up time.
    - Amazon Snapstart is based on this technology 


