# Tournament

```typescript
name: { type: String, unique: true },
maxParticipants: { type: Number, default: 0 },
requisites: { type: Array, default: [] },
startDate: { type: String, default: moment().format('YYYY-MM-DD') },
endDate: { type: String, default: null },
durationDays: { type: Number, default: 0 },
status: { type: String, default: 'Todo', enum: statusValid },
info: { type: String, default: '' },
```
