# Blockchain Based Relationships

The heart of Auth4Flow is it's ability to utilize the blockchain as a security layer, any [Object Type](object-types/) can be related to the status of a users account on the Flow blockchain. This includes tracking ownership of Fungible Tokens or NFTs but can also be triggered by any event being monitored by [Alerts4Flow](../../alerts4flow/event-monitors.md).

To accomplish this we need a system that can verify an account's current status at given times, as well as monitor for events to update access control rights in (mostly) real time.

### Event Based [Warrants](warrants.md) (Relationships)

When creating [Event Monitors](../../alerts4flow/event-monitors.md) you can define `Object` and `Subject` relationships using the same rules as when creating [Warrants](warrants.md). With the ability to mix and match hardcoded values for `ObjectId\SubjectId` or define fields from the emitted event using `ObjectIdField/SubjectIdField,` you can create any sort of realtime gated `users`, `tenants`, `roles`, or other `ObjectTypes`.

See the [API Reference](http://127.0.0.1:5000/s/IcL9vdAZthTfPhyumczL/alerts4flow/event-monitoring/add-event-to-monitor-service) for how to get started. Once the Admin Dashboard is launched you will be able to create gated access rules for pre-defined `ObjectTypes` directly from the dashboard.

### Script Verifiers

Not all events emit the information need to make access control decisions, nor does the above realtime monitoring account for getting the account status of a user during registration or activites that occured during downtime/maintence peirods when Forge4Flow is offline. To account for this a system is being developed so verification Cadence scripts can run at system startup, in response to events, and/or on a defined schedule.
