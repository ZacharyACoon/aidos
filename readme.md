# Aidos, Αἰδώς - Goddess of respect, modesty, and shame. [<sup>wiki</sup>](https://en.wikipedia.org/wiki/Aidos)

# About

This is a moderation toolsetThis is a project of moderation tools to aid in the administration of communities.

# Features

Moderation

- [] Text
  - [] Emojis
- [] Audio
  - [] Quality - Quality of user audio.
    - [] Volume
    - [] Clarity
    - [] Distortion
  - [] Interuption - Users interupting others.
  - [] Disruption
- [] Image


# Conceptual Design

```mermaid
---
config:
flowchart:
subGraphTitleMargin:
top: 10
bottom: 10

---
flowchart TD
subgraph PI[Platform Interfaces]
Discord
Facebook
IRC
Instagram
Slack
TikTok
end

    subgraph Adaptors
        Audio & Image & Video & Link --> Text
    end

    subgraph Classification
        Faith
        Type
        Severity
        Visibility
    end

    subgraph Consideration
        DF[Defined Policy]
        subgraph Context Moderation History
            CMC[Moderation Classifications]
            CMA[Moderation Actions]
        end
        subgraph User Moderation History
            UMC[Moderation Classifications]
            UMA[Moderation Actions]
        end
    end

    subgraph Suggestion
        SMAT[Moderation Action Type]
        SMAD[Moderation Action Duration]
    end

    subgraph Review
        NotifyReviewers[Notify Reviewers] -->
        Accept & Deny([Deny])
    end

    subgraph Action
        Execution
        Notification
    end
    
    subgraph Appeal
        NotifyReviewers[Notify Reviewers]
    end
    
    PI --> 
    Adaptors --> 
    Classification --> 
    Consideration --> 
    Suggestion --> 
    Review -->
    Action --> 
    Appeal

    classDef default subgraphTitleMargin:10;
    classDef pad top:50;
    class PI,Adaptors,Classification,Suggestion pad;
```
