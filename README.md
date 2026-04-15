🚀 Account Rating Filter (LWC)

This project demonstrates filtering Account records by Rating using two different approaches in Lightning Web Components (LWC):

Imperative Apex Call
@wire (Reactive Apex)

It highlights the difference between controlled execution vs reactive data fetching.

📌 Features
Filter Accounts by Rating (Hot, Warm, Cold)
Dynamic UI rendering using SLDS
Badge styling based on rating
Loading spinner for better UX
Empty state handling
Error handling


🧠 Concepts Covered
Lightning Web Components (LWC)
Apex Integration
Imperative vs @wire
Conditional Rendering
Event Handling
Data Transformation (UI mapping)
SLDS Styling
🛠️ Components
1️⃣ accountRatingFilter (Imperative)

Approach: Imperative Apex Call

Data is fetched only when user clicks button
Full control over execution

Better for:
User-triggered actions
Conditional API calls

Key Logic:
getAccounts({ rating: this.rating })


Highlights:
Uses isLoading for spinner control
Handles success, error, and empty states explicitly
Transforms data to include badgeClass
2️⃣ accountRatingFilterWire (Reactive)

Approach: @wire

Data is fetched automatically when rating changes
Reactive and declarative
Less control compared to imperative
Key Logic:
@wire(getAccounts, { rating: '$rating' })
Highlights:
No button required
Automatic refresh on input change
Simpler but less flexible


⚖️ Imperative vs @wire
Feature	Imperative	@wire
Execution Control	✅ Full control	❌ Automatic
Trigger	Button click	Variable change
Use Case	User actions	Reactive UI
Error Handling	Manual	Built-in pattern

🎯 Key Learnings
Imperative calls give better control
@wire provides cleaner reactive design
Proper state handling (loading, empty, error) is critical
UI should not depend on raw backend data → always transform


🚨 Common Mistakes Avoided
❌ Passing '$rating' in imperative call
❌ Using data variable for loading state
❌ Mixing UI states (loading vs empty vs data)
❌ No data transformation for UI styling


📸 UI Highlights
<img width="299" height="244" alt="6" src="https://github.com/user-attachments/assets/4a73313d-fc33-4058-ba27-50f5dc344cde" />
