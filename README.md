1. Project Overview
•	A bilingual (Urdu/English) chatbot application for Punjab Police Khidmat Markaz that provides information about police services using AI-powered responses.
2. Architecture Components
2.1 AI Models & Integration
•	Primary Model: GPT-3.5-turbo (OpenAI)
•	Location: src/services/openai.ts
•	Temperature: 0.7 (balanced creativity/consistency)
•	System Prompt: Configured to respond in Urdu about police services
•	Secondary Model: LangChain Integration
•	Location: src/utils/langchainService.ts
•	Purpose: Enhanced context-aware responses
•	Model: OpenAI with ConversationalRetrievalQAChain
2.2 Data Management
•	Vector Database: ChromaDB
•	Location: src/utils/websiteData.ts
•	Purpose: Stores and retrieves website content
•	Collection: 'punjab_police_data'
2.3 Web Scraping
•	Implementation: scripts/scrapeWebsite.js
•	Technology: Cheerio
•	Target: Punjab Police website (pkm.punjab.gov.pk)
•	Data Collection:
•	Main content
•	Article sections
•	Headers and titles
3. Component Structure
3.1 Core Components
1.	ChatHeader (src/components/ChatHeader.tsx)
•	Purpose: Main application header
•	Features: Branding and title display
2.	ChatInput (src/components/ChatInput.tsx)
•	Purpose: User input handling
•	Features:
•	RTL text support
•	Message submission
•	Loading state management
3.	ChatMessages (src/components/ChatMessages.tsx)
•	Purpose: Message display
•	Features:
•	Message threading
•	Loading indicators
•	Error handling
4.	QuestionSuggestions (src/components/QuestionSuggestions.tsx)
•	Purpose: Predefined questions
•	Categories:
•	Services
•	Complaints
•	Documents
•	Emergency
3.2 Custom Hooks
•	useChat (src/hooks/useChat.ts)
•	Purpose: Chat state management
•	Features:
•	Message handling
•	API integration
•	Error handling



4. Data Flow
User Input → ChatInput
↓
useChat Hook
↓
OpenAI/LangChain Service
↓
ChromaDB (Context)
↓
Response Generation
↓
Message Display
5. Configuration
5.1 OpenAI Configuration
// src/config/openai.ts
model: "gpt-3.5-turbo"
temperature: 0.7
systemPrompt: Urdu-focused police service responses
5.2 Sample Questions
•	Location: src/config/questions.ts
•	Categories: 4 main sections
•	Total Questions: 14 predefined queries
6. Technical Stack
6.1 Frontend
•	React 18.3.1
•	TypeScript
•	Tailwind CSS
•	Vite
6.2 AI/ML
•	OpenAI API
•	LangChain
•	ChromaDB
6.3 Utilities
•	Axios for HTTP requests
•	Cheerio for web scraping
•	Lucide React for icons
7. Code Organization
•	Total Chunks: 15 main code chunks
•	Components (4 files)
•	Services (2 files)
•	Utils (3 files)
•	Hooks (1 file)
•	Types (1 file)
•	Config (2 files)
•	Scripts (1 file)
•	Main App (1 file)
8. Best Practices Implemented
•	Modular component architecture
•	TypeScript for type safety
•	Custom hooks for state management
•	Error boundary implementation
•	RTL support for Urdu language
•	Responsive design
•	Accessibility considerations
9. Future Improvements
•	Implement caching for responses
•	Add more language models
•	Enhance context understanding
•	Expand question database
•	Add voice input support
•	Implement analytics

8. Conclusion
This project is an opportunity to bridge accessibility gaps using a custom chatbot that aligns with modern AI practices. By adhering to structured workflows and leveraging cutting-edge tools, it ensures both depth of knowledge and accuracy of responses while showcasing the potential of language processing for public service.


