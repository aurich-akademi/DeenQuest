# UPKK Adventure

A child-friendly learning application for Malaysian primary school students to learn and practise UPKK-related subjects through storytelling, gamification, quizzes, progress tracking, and adaptive revision.

The application is designed initially for **Year 2 and Year 3** learners, with an architecture that can later support additional school years and subjects.

> Learning flow: **Story → Learn → Explore → Practise → Challenge → Feedback → Reward → Review**

---

## 1. Project Goal

UPKK Adventure is not intended to be a conventional exam portal.

The goal is to create a learning experience that feels like an educational adventure while still providing structured practice, mastery tracking, and revision support.

The application combines:

- Interactive storytelling
- Topic-based learning
- Gamification
- Practice questions
- Quizzes and challenges
- XP, levels, coins, stars, and badges
- Progress tracking
- Weak-topic detection
- Personalised revision
- Parent progress dashboard

---

## 2. Target Users

### Primary Users

Malaysian primary school students.

Initial target:

- Year 2
- Year 3
- Approximately 8–9 years old

### Secondary Users

Parents or guardians who want to monitor:

- learning progress
- quiz performance
- topic mastery
- strong topics
- weak topics
- recent learning activity

---

## 3. Language

Primary interface language:

**Bahasa Malaysia**

The system should also support:

- Jawi
- Arabic text
- Islamic terminology

where required by learning content.

---

## 4. Core Learning Experience

Each topic follows a structured learning journey.

```text
STORY
  ↓
LEARN
  ↓
EXPLORE
  ↓
PRACTISE
  ↓
CHALLENGE
  ↓
FEEDBACK
  ↓
REWARD
  ↓
REVIEW
```

Example:

```text
Topic: Adab Dengan Ibu Bapa

1. Story
2. Think
3. Learn
4. Practice
5. Mini Challenge
6. Reward
7. Reflection
```

The application should prioritise active learning rather than passive reading.

---

## 5. Main Features

### Student Dashboard

The student dashboard may display:

- Greeting
- Student name
- Avatar
- Current level
- XP progress
- Daily streak
- Stars
- Coins
- Daily mission
- Continue learning
- Adventure map
- Recent badges
- Weak topics
- Recommended revision
- Overall progress

---

### Adventure Map

Learning topics are presented as an adventure instead of a standard topic list.

Example learning areas:

```text
Kampung Adab
Masjid Ibadah
Bukit Akidah
Kota Sirah
Pulau Jawi
Arabia Quest
```

Each learning node may have one of these states:

- Locked
- Available
- In Progress
- Completed
- Mastered

The names above are placeholders and should remain configurable.

---

### Interactive Storytelling

Each learning topic can contain a short interactive story.

Recommended length:

**3–6 scenes**

Each scene may include:

- illustration
- narrator text
- character dialogue
- learner choice
- scenario question
- learning point

Stories should be:

- short
- positive
- age appropriate
- culturally appropriate
- relevant to Malaysian Muslim children
- connected to the learning objective

A **Skip Story** option should be available during revision.

---

## 6. Quiz and Question Engine

The reusable question engine should support:

1. Multiple Choice
2. True / False
3. Match the Answer
4. Drag and Drop
5. Arrange in Correct Order
6. Fill in the Blank
7. Image-Based Questions
8. Scenario Questions
9. Jawi Questions
10. Arabic Vocabulary Questions
11. Story Decision Questions

Questions should not only test memorisation.

Where appropriate, include:

- remembering
- understanding
- simple application
- situational reasoning

---

## 7. Question Data Model

Suggested question structure:

```ts
export interface Question {
  id: string;
  year: number;
  subject: string;
  topic: string;
  subtopic?: string;
  difficulty: "easy" | "medium" | "hard";
  questionType:
    | "multiple-choice"
    | "true-false"
    | "matching"
    | "drag-drop"
    | "ordering"
    | "fill-blank"
    | "image"
    | "scenario"
    | "jawi"
    | "arabic-vocabulary"
    | "story-decision";

  question: string;
  options?: string[];
  correctAnswer: string | string[];
  explanation: string;
  hint?: string;
  learningObjective?: string;
  sourceReference?: string;
  reviewStatus: "verified" | "needs_review" | "draft";
}
```

---

## 8. Sample JSON Question

```json
{
  "id": "Y3-ADAB-001",
  "year": 3,
  "subject": "Adab",
  "topic": "Adab Dengan Ibu Bapa",
  "subtopic": "Membantu Ibu Bapa",
  "difficulty": "easy",
  "questionType": "scenario",
  "question": "Ali melihat ibunya membawa banyak barang. Apakah tindakan terbaik?",
  "options": [
    "Membantu membawa barang",
    "Pergi bermain",
    "Membiarkan ibu seorang",
    "Menonton televisyen"
  ],
  "correctAnswer": "Membantu membawa barang",
  "explanation": "Membantu ibu bapa merupakan salah satu contoh adab yang baik.",
  "hint": "Fikirkan cara kita boleh meringankan beban ibu bapa.",
  "learningObjective": "Mengenal pasti contoh adab yang baik terhadap ibu bapa.",
  "sourceReference": "",
  "reviewStatus": "needs_review"
}
```

---

## 9. Gamification

### XP

Example XP rules:

```text
Correct answer        +10 XP
Complete topic        +50 XP
Perfect quiz          Bonus XP
Daily mission         Bonus XP
```

All reward values should be configurable.

---

### Levels

Example levels:

```text
Level 1 — Pelajar Baru
Level 2 — Pencari Ilmu
Level 3 — Sahabat Ilmu
Level 4 — Bintang UPKK
Level 5 — Juara UPKK
```

---

### Stars

Suggested mastery stars:

```text
1 Star  = Completed
2 Stars = Good Mastery
3 Stars = Excellent Mastery
```

---

### Coins

Virtual coins may be used to unlock cosmetic items such as:

- avatar accessories
- outfits
- profile frames
- backgrounds
- badges

No real-money purchases are required.

---

### Badges

Examples:

- Bintang Sirah
- Jaguh Jawi
- Hebat Ibadah
- Sahabat Adab
- Pakar Akidah
- Arabic Explorer
- 7-Day Streak
- Perfect Score

---

## 10. Mastery System

Suggested mastery interpretation:

| Score | Status |
|---|---|
| 0–39% | Perlu Bimbingan |
| 40–59% | Sedang Belajar |
| 60–79% | Baik |
| 80–89% | Sangat Baik |
| 90–100% | Dikuasai |

Mastery should be calculated from cumulative performance instead of a single attempt.

---

## 11. Smart Revision

The MVP can use rule-based adaptive learning.

Track:

- incorrect answers
- topic accuracy
- number of attempts
- recent performance
- incomplete topics

Example:

```text
Misi Hari Ini:
Kuasai Wuduk
```

Suggested revision flow:

```text
1 short explanation
1 mini story
3 practice questions
1 challenge
```

The architecture should allow AI-based personalisation to be added later.

---

## 12. Practice Modes

Supported practice modes:

- Quick Practice
- Topic Practice
- Weak Topic Practice
- Mixed Practice

Suggested question counts:

- 5 questions
- 10 questions
- 20 questions

---

## 13. Challenge Modes

Possible challenge modes:

- Mini Challenge
- Subject Challenge
- Weekly Challenge
- Mock Assessment
- Boss Challenge

During challenge or assessment mode:

- answers are not revealed immediately
- final score is shown after completion
- answer review is available afterwards

Practice mode should provide immediate feedback.

---

## 14. Parent Dashboard

Parents should be able to view:

- child profile
- learning time
- completed topics
- subject progress
- quiz scores
- accuracy
- strengths
- weak topics
- recent learning activity
- badges and achievements
- revision recommendations

Example:

```text
Sirah   82%
Ibadah  71%
Jawi    55%
Adab    90%
```

Recommendation:

```text
Perlu perhatian: Jawi
```

---

## 15. Suggested Tech Stack

Preferred stack:

```text
Next.js
React
TypeScript
Tailwind CSS
shadcn/ui
Lucide Icons
Recharts
Framer Motion
```

For MVP persistence:

```text
localStorage
```

Future database options:

```text
Supabase
PostgreSQL
Firebase
```

The application should use a data abstraction layer so the storage system can be changed later without rewriting the main application.

---

## 16. Suggested Routes

```text
/
├── /dashboard
├── /adventure
├── /subject/[subjectId]
├── /topic/[topicId]
├── /story/[storyId]
├── /practice
├── /practice/[topicId]
├── /quiz/[quizId]
├── /challenge
├── /achievements
├── /profile
├── /parent
└── /settings
```

---

## 17. Suggested Folder Structure

```text
upkk-adventure/
│
├── app/
│   ├── page.tsx
│   ├── dashboard/
│   ├── adventure/
│   ├── subject/
│   ├── topic/
│   ├── story/
│   ├── practice/
│   ├── quiz/
│   ├── challenge/
│   ├── achievements/
│   ├── profile/
│   ├── parent/
│   └── settings/
│
├── components/
│   ├── ui/
│   ├── dashboard/
│   ├── quiz/
│   ├── story/
│   ├── adventure/
│   ├── gamification/
│   └── parent/
│
├── data/
│   ├── year2/
│   │   ├── subjects/
│   │   ├── topics/
│   │   ├── questions/
│   │   └── stories/
│   │
│   └── year3/
│       ├── subjects/
│       ├── topics/
│       ├── questions/
│       └── stories/
│
├── lib/
│   ├── quiz/
│   ├── gamification/
│   ├── mastery/
│   ├── progress/
│   └── storage/
│
├── types/
│   ├── question.ts
│   ├── student.ts
│   ├── progress.ts
│   └── achievement.ts
│
├── public/
│   ├── images/
│   ├── avatars/
│   ├── badges/
│   └── illustrations/
│
├── README.md
├── package.json
├── tsconfig.json
└── tailwind.config.ts
```

---

## 18. Important Utility Functions

Recommended business logic functions:

```ts
calculateXP()
calculateLevel()
calculateMastery()
updateStreak()
awardBadge()
selectAdaptiveQuestions()
calculateQuizScore()
updateTopicProgress()
generateDailyMission()
```

Business logic should remain separate from UI components.

---

## 19. Content Source Workflow

Past Year 2 and Year 3 questions will be used as reference material.

Recommended processing flow:

```text
Uploaded Questions
      ↓
Content Extraction
      ↓
Year
      ↓
Subject
      ↓
Topic
      ↓
Subtopic
      ↓
Learning Objective
      ↓
Question Type
      ↓
Difficulty
      ↓
Question Bank
```

The uploaded material should guide:

- curriculum scope
- terminology
- difficulty
- wording
- topic structure
- question style

Do not blindly copy source questions.

Create new practice questions based on the same learning objectives and expected learner level.

---

## 20. Islamic Content Verification

Religious accuracy is a critical requirement.

Do not fabricate:

- Quran verses
- Hadith
- religious rulings
- Arabic meanings
- Islamic historical events

Every content item should support:

```ts
reviewStatus:
  | "verified"
  | "needs_review"
  | "draft"
```

Content should preferably distinguish between:

```text
SOURCE-VERIFIED CONTENT
AI-GENERATED PRACTICE CONTENT
```

Unverified religious claims should never be presented as authoritative.

---

## 21. Adding New Questions

Add questions inside the relevant year folder.

Example:

```text
data/year3/questions/adab.json
```

Example content:

```json
[
  {
    "id": "Y3-ADAB-001",
    "year": 3,
    "subject": "Adab",
    "topic": "Adab Dengan Ibu Bapa",
    "difficulty": "easy",
    "questionType": "multiple-choice",
    "question": "Apakah contoh adab yang baik terhadap ibu bapa?",
    "options": [
      "Membantu mereka",
      "Mengabaikan mereka",
      "Bercakap kasar",
      "Tidak mendengar nasihat"
    ],
    "correctAnswer": "Membantu mereka",
    "explanation": "Membantu ibu bapa merupakan contoh akhlak dan adab yang baik.",
    "reviewStatus": "needs_review"
  }
]
```

The application should automatically read new question data without requiring changes to core quiz logic.

---

## 22. Future Question Import

Planned import support:

```text
JSON
CSV
Excel
```

MVP requirement:

**JSON import**

Future admin tools may allow:

- Add question
- Edit question
- Delete question
- Bulk import
- Filter by year
- Filter by subject
- Filter by topic
- Review question status
- View question performance

---

## 23. UI / UX Direction

Design style:

- modern
- clean
- colourful
- child-friendly
- Islamic-friendly
- playful
- professional

Avoid:

- overcrowded screens
- tiny fonts
- excessive animations
- generic corporate dashboards
- preschool-looking designs

Use:

- rounded cards
- large buttons
- clear icons
- progress indicators
- friendly illustrations
- micro-interactions
- simple navigation

Primary device priority:

**Tablet**

Also support:

- Desktop
- Mobile

---

## 24. Accessibility

Important requirements:

- readable fonts
- high contrast
- large touch targets
- clear correct/incorrect states
- keyboard support where applicable
- simple navigation
- minimal reading overload

Future-ready feature:

```text
Read Aloud / Audio Support
```

---

## 25. Demo Profile

Suggested demo account:

```text
Name: Alya
Year: Year 3
```

Populate sample progress so the dashboard, mastery system, badges, and parent analytics can be demonstrated.

---

## 26. Development Phases

Recommended development sequence:

### Phase 1
Analyse Year 2 and Year 3 sample questions.

### Phase 2
Create content taxonomy and data model.

### Phase 3
Build application architecture.

### Phase 4
Build reusable design system.

### Phase 5
Build student dashboard.

### Phase 6
Build adventure map.

### Phase 7
Build storytelling engine.

### Phase 8
Build quiz engine.

### Phase 9
Build gamification.

### Phase 10
Build mastery and progress tracking.

### Phase 11
Build parent dashboard.

### Phase 12
Populate seed content.

### Phase 13
Test and refine.

---

## 27. Testing Checklist

Test the following:

- navigation
- profile selection
- quiz answering
- score calculation
- XP calculation
- level progression
- coin rewards
- badges
- mastery calculation
- topic completion
- streak tracking
- weak-topic detection
- quiz retry
- question randomisation
- local persistence
- browser refresh
- responsive layouts
- empty states
- error states
- console errors

---

## 28. MVP Priority

If the project scope becomes too large, prioritise:

```text
1. Student Profile
2. Dashboard
3. Subject / Topic Navigation
4. Story Learning
5. Question Engine
6. Practice Mode
7. Quiz Mode
8. Scoring
9. XP and Levels
10. Progress Tracking
11. Adventure Map
12. Badges
13. Parent Dashboard
```

A smaller working application is better than a large unfinished one.

---

## 29. Getting Started

### Install dependencies

```bash
npm install
```

### Run development server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

## 30. Build for Production

```bash
npm run build
npm start
```

---

## 31. Product Vision

The application should feel like:

```text
Microlearning
+
Interactive Islamic Learning
+
Adventure Game Progression
+
UPKK Practice
```

It should **not** feel like:

```text
Google Form
Static Quiz Website
Generic LMS
Spreadsheet-Based Question Bank
```

The priority is:

> **Learning value first. Gamification second.**

Gamification should motivate learning, not distract from it.

---

## 32. Future Roadmap

Possible future features:

- Year 4 and Year 5 content
- AI-generated adaptive practice
- AI explanation assistant
- Text-to-speech
- Arabic pronunciation
- Teacher dashboard
- School leaderboard
- Class management
- Assignment mode
- Question analytics
- Spaced repetition
- Cloud sync
- Supabase authentication
- Multi-child parent accounts
- PWA installation
- Offline learning
- Push notifications
- Printable revision reports

---

## 33. Development Principle

When building this project:

> Do not stop at planning.

Implement the simplest functional version of each important feature.

Avoid leaving major functionality as placeholder-only components or unfinished TODO items.

After implementation:

1. run the application,
2. check for errors,
3. repair broken flows,
4. verify question logic,
5. verify saved progress,
6. test responsiveness.

---

## License

To be determined.

---

## Project Status

**Status:** Early Development / MVP

Initial content will be based on verified Year 2 and Year 3 reference questions supplied by the project owner.
