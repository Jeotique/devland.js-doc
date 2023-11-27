---
description: Emitted when members were added or removed from a thread
---

# threadMembersUpdate

```javascript
bot.on("threadMembersUpdate", (data) => {
    console.log(`Thread ${data.id} on guild ${data.guild.name} has been updated`)
    const addedMembers = data.added_members
    const removedMembers = data.removed_rembers
    if (addedMembers.length > 0) {
        console.log(`Added members : ${addedMembers.map(member => member.user.tag).join(", ")}`)
    }
    if (removedMembers.length > 0) {
        console.log(`Removed members : ${removedMembers.map(memberId => memberId).join(", ")}`)
    }
    console.log(`Total thread members : ${data.member_count}`)
})
```

