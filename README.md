##Component Orchestration with Behavior Trees

The blue component is chasing the green ones (opportunities) which are static and needs to avoid the red component which is chasing it (threat).

While behavior trees are used in game development, business applications could also benefit from such a standard.

![ ](./screen.png)

### Tree Definition

```

                    new b3.Sequence({
                        children: [
                            new b3.Priority({
                                children: [
                                    new b3.Sequence({
                                        children: [
                                            new ThreatDetected(),
                                            new AvoidThreat()
                                        ]
                                    }),
                                    new b3.Sequence({
                                        children: [
                                            new SeekOpportunity(),
                                            new TakeOpportunity()
                                        ]
                                    })]
                            }),
                            new SeekSubject()]
                    });
```

###References

[https://github.com/andoco/objc-behaviortree](https://github.com/andoco/objc-behaviortree)

[https://github.com/renatopp/behavior3js](https://github.com/renatopp/behavior3js)