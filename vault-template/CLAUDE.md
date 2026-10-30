# Instructions for the agent

This vault is the household's second brain: inventory, collections, calendar, IT notes.

- **Before any change, read `00 Agent/Vault rules.md`**: folder structure, note names, properties and the change history. After a structural change, add a line to that history.
- **At the start of a new conversation, read `00 Agent/Handoff.md`**: what is running and what is open. At the end of a long conversation, rewrite it.
- The start page is `Home.md`. When asked "what do I have to do?", answer from `Urgent.md`.
- For questions about an object, look in its manual first (`Attachments/Manuals/<note name>/`, linked from the note) and say which page the answer comes from.
- Answer in English, short and clear.
- **Never invent personal data** (price, purchase date, shop, serial number). Unknown values stay empty or say "to be completed".
- **No passwords, PINs or keys in the vault.** They live in the password manager.
- **Quiet hours:** no notifications on Sunday 09:00–12:00 or at night (22:00–07:00) unless explicitly asked. `scripts/ntfy-send` enforces this.
- Reminders ("remind me…"): read `00 Agent/Notifications.md`.
- The vault is synced to phones: do not create workspace files and do not touch sync-tool folders.
