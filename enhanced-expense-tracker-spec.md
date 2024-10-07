# Expense Tracker

## 1. Data Structure

### Expense Model
```typescript
interface Expense {
  id: string;
  category: string;
  item: string;
  quantity: number;
  unitPrice: number;
  total: number;
  status: 'PAID' | 'PENDING' | 'SKIPED' | 'CANCELED';
  paid: number;
  date: Date;
  type: 'YEARLY' | 'MONTHLY' | 'WEEKLY' | 'DAILY' | 'ONE_TIME';
  isObligatory: boolean;
}
```

### Income Model
```typescript
interface Income {
  id: string;
  source: string;
  amount: number;
  date: Date;
  isRecurring: boolean;
}
```

## 2. Core Features

### Expense Management
- CRUD operations for expenses
- Categorization: Entertainment, Work, Internet Provider, Personal, etc.
- Status tracking (with colors like Tags): PAID, PENDING, SKIPED, CANCELED
- Distinguish between Monthly and One-Time expenses
- Mark expenses One-Time as Obligatory or Optional

### Income Tracking
- Add and manage income sources
- Support for recurring and one-time income entries

### Dashboard
- Overview of total monthly expenses
- Breakdown of obligatory and optional one-time expenses
- Display of total income and remaining balance
- Visualization of expenses by category (pie chart)
- Expense trends over time (line chart)

### Filtering and Sorting
- Filter expenses by:
  - Type (Monthly/One-Time)
  - Category
  - Status
  - Date range
- Sort expenses by status, amount, date, or category

## 3. Advanced Features

### Budget Planning
- Set monthly budgets for each category
- Visual indicators for budget status

### Expense Prioritization
- Drag-and-drop interface for manual prioritization
- Auto-prioritization based on due dates and obligation status

### Recurring Transactions
- Automate recurring expenses (e.g., subscriptions)
- Set up recurring income entries

### Financial Goals
- Set savings goals
- Track progress towards goals

## 4. User Interface

### Modern Dashboard
- Clean, intuitive layout
- Dark/light mode toggle
- Responsive design for mobile and desktop

### Expense List View
- Tabular view similar to Excel format
- Inline editing for quick updates
- Collapsible sections for Monthly and One-Time expenses

### Data Visualization
- Interactive charts for expense distribution
- Trend analysis for spending patterns

## 5. Additional Enhancements

### Data Export
- Export reports in various formats

### Notifications
- Reminders for upcoming payments
- Alerts for exceeding budget limits

### Receipt Management
- Upload and attach receipts to expenses
- OCR functionality for automatic data extraction

## 6. Technical Considerations

### Frontend
- Next.js with TypeScript
- Tailwind CSS for styling
- React Query for state management
- Recharts or D3.js for data visualization

### Backend
- Next.js API routes
- MongoDB for data storage
- NextAuth.js for authentication

### Deployment
- Vercel for hosting
- MongoDB Atlas for database

Remember to implement proper error handling, data validation, and security measures throughout the application.
