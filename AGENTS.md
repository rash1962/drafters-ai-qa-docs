# Drafters AI Agent Guide

This document provides project-specific instructions for AI agents used for QA and automation.

# AGENTS.md

# Drafters AI Agent Operating Manual

## Purpose

This document provides project-specific instructions for AI agents working on the Drafters platform. It serves as the primary knowledge source for AI-assisted development, QA, and automation testing.

The information in this document includes business rules, QA processes, coding standards, testing guidelines, and project-specific workflows that cannot be inferred directly from the source code.

AI agents should always use this document before generating code, test cases, reviewing pull requests, or performing automation-related tasks.

---

# 1. Project Information

## Project Name

Drafters Fantasy Sports Platform

## Project Overview

Drafters is a fantasy sports platform that allows users to create fantasy lineups, participate in contests, draft players, complete Pick'em entries, manage wallets, complete identity verification (KYC), and compete for prizes across multiple sports.

The platform supports Web, Android, iOS, and an Admin Portal used for contest management, user management, payment configuration, reporting, and operational tasks.

## Project Objectives

- Provide a secure fantasy sports platform.
- Support real-money contests.
- Enable multiple fantasy game formats.
- Provide reliable payment processing.
- Maintain fair gameplay.
- Deliver a consistent user experience across all platforms.

## Supported Platforms

- Web
- Android
- iOS
- Admin Portal

## Target Users

### End Users

- Fantasy Sports Players

### Internal Users

- QA Engineers
- Developers
- Product Managers
- Customer Support
- Operations Team
- Administrators

## Major Functional Areas

- User Registration
- Authentication
- Profile Management
- Identity Verification (KYC)
- Wallet
- Payments
- Contest Management
- Draft
- Pick'em
- Props
- Rankings
- Leaderboards
- Notifications
- Responsible Gaming
- Promotions
- Admin Portal

## Technology Stack

### Frontend

- Angular (Web)

### Mobile

- Android-kotlin
- iOS-swift

### Backend

- NestJS
- nodeJS
- php

### Database

- MongoDB
- mysql

### Cache

- Redis

### Cloud

- AWS

## AI Agent Scope

This repository is intended to support AI-assisted:

- Manual QA
- Test Case Generation
- Playwright automation
- Appium Automation
- API Test Generation
- Regression Analysis
- Pull Request Review
- Bug Analysis
- Documentation
- Automation Maintenance

The AI agent must always follow the documented business rules and QA standards contained in this repository.


# 2. Repository Structure

## Overview

This repository serves as the central knowledge base for AI-assisted QA, test automation, and project documentation for the Drafters platform.

The repository is organized to help AI agents quickly locate project documentation, business rules, feature flows, testing standards, and automation guidelines.

```
drafters-ai-qa-docs/
│
├── README.md
├── AGENTS.md
│
├── flows/
├── automation/
├── api/
├── test-data/
└── reports/
```

---

## Directory Details

### AGENTS.md

The primary instruction document for AI agents.

Contains:

- Project overview
- Business rules
- QA guidelines
- Coding standards
- Deployment workflow
- AI responsibilities
- Safety rules
- Reporting standards

AI agents should always read this document before generating code, automation scripts, or QA reports.

---

### flows/

Contains feature-wise documentation.

Each module should have its own Markdown file describing:

- Feature overview
- User journey
- Business rules
- Test scenarios
- Expected behavior
- Edge cases
- Validation points
- Automation considerations

Examples:

```
flows/
├── authentication.md
├── registration.md
├── login.md
├── kyc.md
├── wallet.md
├── finix-payment.md
├── contest.md
├── draft.md
├── pickem.md
├── props-booster.md
├── ranking.md
├── responsible-gaming.md
├── notifications.md
└── profile.md
```

---

### automation/

Contains automation standards and implementation guidelines.

Examples include:

- Appium framework standards
- Page Object Model (POM) guidelines
- Locator strategy
- Coding standards
- Naming conventions
- Reusable utilities

---

### api/

Contains API-related documentation.

Each API document should include:

- Endpoint information
- Request parameters
- Response structure
- Validation rules
- Error handling
- Authentication requirements

---

### test-data/

Contains testing resources such as:

- Test accounts
- Sample datasets
- Test scenarios
- Environment-specific test configurations

No production credentials or sensitive information should be stored in this directory.

# 3. Development Environment

## Overview

The Drafters platform consists of Web, Android, iOS, Backend, and Admin Portal applications.

QA testing is primarily performed using dedicated staging environments. Local development setup is typically used by the development team, while QA validates features using deployed staging builds and production build.

---

## Web Application

Environment:
- Staging
- Production

QA Activities:
- Functional Testing
- Regression Testing
- Cross-browser Testing
- UI/UX Validation
- API Verification
- Console Log Verification

---

## Android Application

Build Distribution:
- Staging APK
- production APK

QA Activities:
- Functional Testing
- Regression Testing
- UI Validation
- Deep Link Testing
- Push Notification Testing
- Payment Flow Validation

---

## iOS Application

Build Distribution:
- Staging IPA
- TestFlight (production)

QA Activities:
- Functional Testing
- Regression Testing
- User Journey Validation
- Payment Flow Validation
- Push Notification Testing
- Email Journey Verification

---

## Admin Portal

Environment:
- Staging

QA Activities:
- Feature Configuration
- Contest Management
- Payment Configuration
- Responsible Gaming Configuration
- User Management
- Reporting Validation

---

## Backend Services

Backend services are deployed to staging environments and are validated through:

- API Testing
- Database Verification
- Log Analysis
- Integration Testing

---

## AI Agent Instructions

AI agents should assume that testing is performed against the latest available staging environment unless explicitly instructed otherwise.

Do not assume that local development environments are available.

Always reference the appropriate environment before generating test cases or automation scripts.

Never perform destructive operations against production environments.

# 4. Environment URLs

## Overview

The Drafters platform is deployed across multiple environments. Actual URLs are managed securely and should not be stored in this repository.

AI agents should use the appropriate environment provided by the QA or development team.

---

## Development Environment

| Component | URL |
|-----------|-----|
| Web | `<DEV_WEB_URL>` |
| Backend API | `<DEV_API_URL>` |
| Admin Portal | `<DEV_ADMIN_URL>` |

---

## Staging Environment

| Component | URL |
|-----------|-----|
| Web | `<STAGING_WEB_URL>` |
| Backend API | `<STAGING_API_URL>` |
| Admin Portal | `<STAGING_ADMIN_URL>` |
| Android | `<STAGING_ANDROID_BUILD>` |
| iOS | `<TESTFLIGHT_STAGING_BUILD>` |

---

## Production Environment (Reference Only)

| Component | URL |
|-----------|-----|
| Web | `<PRODUCTION_WEB_URL>` |
| Backend API | `<PRODUCTION_API_URL>` |
| Admin Portal | `<PRODUCTION_ADMIN_URL>` |

---

## Security Guidelines

- Never store production URLs, credentials, or API keys directly in this repository.
- Environment-specific values should be obtained from the organization's secure configuration or secret management system.
- AI agents must never perform destructive operations against production environments.

---

### reports/

Contains QA reporting templates.

Examples:

- Test execution reports
- Regression reports
- AI-generated QA reports
- Bug summary templates
- Automation execution reports

---

## AI Agent Navigation

When performing tasks, AI agents should use the repository in the following order:

1. Read `AGENTS.md` to understand the project context and standards.
2. Read the relevant file under `flows/` to understand the specific feature.
3. Refer to `api/` when API behavior or validation is required.
4. Follow `automation/` guidelines when generating or reviewing automation code.
5. Use `test-data/` for valid test inputs.
6. Generate outputs using the templates available in `reports/`.

## Documentation Maintenance

- Keep documentation up to date with every feature enhancement or business rule change.
- Create a new module document whenever a new feature is introduced.
- Remove obsolete documentation after feature deprecation.
- Ensure all documentation remains synchronized with the latest application behavior.

# 5. Authentication

## Overview

The Drafters platform requires user authentication before accessing protected features such as Wallet, Contests, Draft, Profile, and Payments.

Authentication is role-based and varies depending on the platform (Web, Mobile, or Admin Portal).

---

## Authentication Methods

### Web Application

- Login using registered email and password.
- Session is established after successful authentication.
- Authenticated users can access protected modules based on their permissions.

### Mobile Application (Android & iOS)

- Login using registered email and password.
- Authentication session is maintained until logout or session expiration.
- Users must be authenticated before accessing restricted features.

### Admin Portal

- Admin users authenticate using administrator credentials.
- Access is restricted based on assigned roles and permissions.

---

## User Roles

### End User

Permissions:

- Register an account
- Login
- Complete KYC
- Add Funds
- Join Contests
- Draft Players
- Participate in Pick'em
- View Rankings
- Manage Profile

---

### Administrator

Permissions:

- Manage Contests
- Configure Promotions
- Manage Users
- View Reports
- Configure Responsible Gaming
- Manage Payment Settings

---

### QA User

Permissions:

- Validate application functionality
- Execute test scenarios
- Verify business rules
- Access staging environments using approved QA accounts

---

## Authentication Validation Checklist

AI agents should verify:

- Successful login with valid credentials.
- Proper error message for invalid credentials.
- Protected screens require authentication.
- Logout invalidates the active session.
- Unauthorized users cannot access protected resources.
- Session expiration is handled correctly.
- User role permissions are enforced.

---

## Security Guidelines

- Never store usernames or passwords in this repository.
- Never include production credentials.
- Use QA or staging accounts for testing.
- Credentials should be managed through secure secret management systems or environment variables.

---

## AI Agent Instructions

When generating test cases or automation:

- Use only approved QA test accounts.
- Do not hardcode credentials in automation scripts.
- Validate both positive and negative authentication scenarios.
- Verify appropriate error messages for authentication failures.
- Confirm role-based access control is functioning as expected.

# 6. Business Domains

## Overview

The Drafters platform is divided into multiple business domains that collectively deliver the fantasy sports experience across Web, Android, iOS, and the Admin Portal.

Each domain has its own business rules, workflows, APIs, and validation requirements. AI agents must understand the purpose of each domain before generating automation, reviewing code, or analyzing defects.

Detailed documentation for each module is maintained in the `flows/` directory.

---

## 6.1 Authentication

**Purpose**

Manages user authentication and secure access to the platform.

**Responsibilities**

- User Login
- Session Management
- Password Reset
- Logout
- Role-Based Access Control

**Platforms**

- Web
- Android
- iOS
- Admin Portal

**Reference**

`flows/authentication.md`

---

## 6.2 Registration

**Purpose**

Allows new users to create an account and begin onboarding.

**Responsibilities**

- User Registration
- Email Verification
- Terms & Conditions Acceptance
- Initial Account Creation

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/registration.md`

---

## 6.3 User Profile

**Purpose**

Allows users to manage their personal information and account settings.

**Responsibilities**

- View Profile
- Edit Profile
- Account Settings
- Preferences

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/profile.md`

---

## 6.4 Identity Verification (KYC)

**Purpose**

Verifies user identity to meet regulatory and compliance requirements.

**Responsibilities**

- Identity Verification
- Document Validation
- Verification Status
- Compliance Checks

**Platforms**

- Web
- Android
- iOS
- Admin Portal

**Reference**

`flows/kyc.md`

---

## 6.5 Wallet

**Purpose**

Manages user funds and transaction history.

**Responsibilities**

- Wallet Balance
- Deposits
- Withdrawals
- Transaction History
- Bonus Credits

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/wallet.md`

---

## 6.6 Payments

**Purpose**

Processes secure financial transactions.

**Responsibilities**

- Finix Payment Gateway
- PayPal
- Credit & Debit Cards
- Payment Validation
- 3DS Authentication

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/finix-payment.md`

---

## 6.7 Contest Management

**Purpose**

Allows users to browse, join, and manage fantasy contests.

**Responsibilities**

- Contest Lobby
- Contest Details
- Contest Entry
- Contest Rules

**Platforms**

- Web
- Android
- iOS
- Admin Portal

**Reference**

`flows/contest.md`

---

## 6.8 Draft

**Purpose**

Supports player drafting during fantasy contests.

**Responsibilities**

- Draft Room
- Player Selection
- Pick Timer
- Auto Pick
- Draft Queue

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/draft.md`

---

## 6.9 Pick'em

**Purpose**

Allows users to create prediction-based fantasy entries.

**Responsibilities**

- Pick Selection
- Entry Submission
- Live Picks
- Pick History
- Result Settlement

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/pickem.md`

---

## 6.10 Props Booster

**Purpose**

Provides promotional boosters that increase potential winnings based on configured rules.

**Responsibilities**

- Booster Eligibility
- Bonus Calculation
- Promotional Rules
- Reward Distribution

**Platforms**

- Web
- Android
- iOS
- Admin Portal

**Reference**

`flows/props-booster.md`

---

## 6.11 Best Ball Survival

**Purpose**

Supports survival-style fantasy contests where entries advance or are eliminated based on weekly performance.

**Responsibilities**

- Weekly Advancement
- Elimination Rules
- Survival Leaderboard
- Final Rankings

**Platforms**

- Web
- Android
- iOS
- Admin Portal

**Reference**

`flows/best-ball-survival.md`

---

## 6.12 Rankings & Leaderboards

**Purpose**

Displays rankings and standings for players, contests, and fantasy competitions.

**Responsibilities**

- Contest Rankings
- Player Rankings
- Leaderboards
- Season Standings

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/ranking.md`

---

## 6.13 Notifications

**Purpose**

Delivers important updates and promotional messages to users.

**Responsibilities**

- Push Notifications
- Email Notifications
- In-App Notifications
- Promotional Campaigns

**Platforms**

- Web
- Android
- iOS

**Reference**

`flows/notifications.md`

---

## 6.14 Responsible Gaming

**Purpose**

Ensures compliance with responsible gaming policies and user protection requirements.

**Responsibilities**

- Deposit Limits
- Spending Limits
- Account Restrictions
- Compliance Rules

**Platforms**

- Web
- Android
- iOS
- Admin Portal

**Reference**

`flows/responsible-gaming.md`

---

## 6.15 Admin Portal

**Purpose**

Provides administrative capabilities for managing the Drafters platform.

**Responsibilities**

- Contest Management
- User Management
- Payment Configuration
- Promotions
- Reporting
- Responsible Gaming Configuration
- Feature Management

**Platforms**

- Admin Portal

**Reference**

`flows/admin-panel.md`

---

## AI Agent Responsibilities

Before generating code, automation scripts, test cases, or reviewing pull requests, AI agents must:

1. Identify the relevant business domain.
2. Read the corresponding documentation under the `flows/` directory.
3. Follow documented business rules and QA standards.
4. Avoid assumptions about undocumented functionality.
5. Request clarification when business requirements are incomplete or ambiguous.

# 7. Business Rules

## Overview

Business rules define the expected behavior of the Drafters platform. AI agents must follow these rules when generating automation tests, reviewing code, analyzing defects, or validating application behavior.

AI agents must never assume business behavior that is not documented.

---

## 7.1 Authentication

### Rules

- Users must register before accessing protected features.
- Only authenticated users can access Wallet, Contests, Draft, Pick'em, and Profile.
- Invalid credentials must display an appropriate error message.
- User sessions must expire according to platform configuration.
- Logout must invalidate the active session.

---

## 7.2 Registration

### Rules

- Every account must have a unique email address.
- Required fields must be validated before registration.
- Registration must not create duplicate accounts.
- Email verification may be required before accessing certain features.
- Users must accept Terms & Conditions before registration.

---

## 7.3 KYC

### Rules

- Users must complete KYC where required by business regulations.
- Verification status must be updated after successful verification.
- Failed verification must not grant restricted access.
- Users cannot bypass mandatory KYC requirements.

---

## 7.4 Wallet

### Rules

- Wallet balance must never become negative.
- Successful deposits must update the wallet balance.
- Failed deposits must not update the wallet balance.
- Every successful transaction must appear in Transaction History.
- Transaction amounts must be recorded accurately.

---

## 7.5 Payments

### Rules

- Payment processing must validate all required fields.
- Failed payments must not create wallet credit.
- Successful payments must update wallet balance.
- Payment errors must display meaningful messages.
- Duplicate payment requests should not create duplicate transactions.
- Sensitive payment information must never be exposed.

---

## 7.6 Contest

### Rules

- Users can join only contests for which they are eligible.
- Entry fees must be deducted only after successful contest entry.
- Contest rules must be displayed before joining.
- Contest status must update correctly.

---

## 7.7 Draft

### Rules

- Draft starts only when contest conditions are satisfied.
- Players cannot be selected more than once within the same draft.
- Auto Pick occurs when the user does not make a selection before the timer expires.
- Draft order must follow contest rules.
- Draft results must be saved correctly.

---

## 7.8 Pick'em

### Rules

- Users must complete all required selections before submitting an entry.
- Submitted entries cannot be modified after confirmation unless supported by business rules.
- Results must be calculated according to official scoring rules.

---

## 7.9 Props Booster

### Rules

- Booster eligibility must follow configured business rules.
- Bonus calculations must be accurate.
- Expired boosters must not be available.
- Users must clearly see booster terms and conditions.

---

## 7.10 Rankings

### Rules

- Rankings must be calculated using official scoring.
- Leaderboards must update after scoring changes.
- Users should only see data they are authorized to access.

---

## 7.11 Notifications

### Rules

- Notifications must be delivered only to eligible users.
- Duplicate notifications should be avoided.
- Notification content must match the triggering event.

---

## 7.12 Responsible Gaming

### Rules

- Deposit limits must be enforced.
- Users exceeding configured limits must be restricted.
- Responsible Gaming settings must be applied consistently across supported platforms.

---

## AI Agent Instructions

When generating automation or reviewing functionality:

- Follow documented business rules.
- Do not infer undocumented behavior.
- Report any conflicts between implementation and documented business rules.
- Raise clarification requests if requirements are ambiguous.

# 8. Frontend QA Guidelines

## Overview

The Drafters platform is available on Web, Android, and iOS. All frontend features must provide a consistent, reliable, and user-friendly experience across supported platforms.

AI agents should follow these QA guidelines when generating automation scripts, reviewing UI changes, or validating feature implementations.

---

## Supported Platforms

- Web
- Android
- iOS

---

## General QA Checklist

The following validations should be performed for every feature unless otherwise specified.

### Functional Validation

- Verify all user actions complete successfully.
- Verify business rules are correctly implemented.
- Verify all validations and error messages.
- Verify success messages where applicable.
- Verify navigation between screens.

---

### UI Validation

- Verify layout consistency.
- Verify fonts, icons, colors, and spacing.
- Verify images and assets load correctly.
- Verify responsive behavior on supported screen sizes.
- Verify dark/light mode if supported.
- Verify platform-specific UI guidelines are followed.

---

### Navigation Validation

Verify:

- Correct screen navigation
- Back navigation
- Deep links (where applicable)
- External links
- Menu navigation
- Bottom navigation
- Tab navigation

---

### API Validation

Verify:

- No failed API requests.
- Correct HTTP status codes.
- Correct response payload.
- Correct error handling.
- Proper loading indicators during API calls.

---

### Performance Validation

Verify:

- Loading indicators appear when required.
- Loading indicators disappear after completion.
- No excessive loading delays.
- Smooth scrolling and animations.
- No UI freezes.

---

### Error Handling

Verify:

- Meaningful validation messages.
- Network failure handling.
- Timeout handling.
- Empty state handling.
- Retry functionality where supported.

---

### Console & Log Validation

For Web:

Verify:

- No JavaScript errors.
- No Console Errors.
- No Failed Network Requests.
- No Broken Resources.

For Mobile:

Verify:

- No Application Crashes.
- No Unexpected Exceptions.
- No ANR (Android Not Responding).
- No iOS Crash Logs.

---

## Core User Journeys

AI agents should prioritize validation of the following business-critical user journeys.

### Authentication

Entry Point

- Login Screen

User Actions

- Login
- Logout
- Forgot Password

Expected Results

- Successful authentication
- Proper session creation
- Appropriate validation messages

Reference

flows/authentication.md

---

### Registration

Entry Point

- Registration Screen

User Actions

- Create Account
- Verify Email
- Accept Terms

Expected Results

- Successful account creation
- Proper validations
- Email verification

Reference

flows/registration.md

---

### KYC

Entry Point

- Verification Screen

User Actions

- Submit documents
- Complete verification

Expected Results

- Verification status updates correctly
- Appropriate validation messages

Reference

flows/kyc.md

---

### Wallet

Entry Point

- Wallet Screen

User Actions

- Deposit Funds
- Withdraw Funds
- View Transaction History

Expected Results

- Balance updates correctly
- Transactions recorded
- Proper success and error handling

Reference

flows/wallet.md

---

### Payments

Entry Point

- Add Funds

User Actions

- Add Card
- Complete Payment
- 3DS Authentication

Expected Results

- Payment processed correctly
- Wallet updated
- Transaction history updated

Reference

flows/finix-payment.md

---

### Contest

Entry Point

- Contest Lobby

User Actions

- Browse Contests
- View Details
- Join Contest

Expected Results

- Contest joined successfully
- Entry fee deducted correctly

Reference

flows/contest.md

---

### Draft

Entry Point

- Draft Room

User Actions

- Join Draft
- Select Player
- Auto Pick

Expected Results

- Draft progresses correctly
- Player selection follows business rules

Reference

flows/draft.md

---

### Pick'em

Entry Point

- Pick'em Lobby

User Actions

- Select Picks
- Submit Entry

Expected Results

- Entry submitted successfully
- Picks displayed correctly

Reference

flows/pickem.md

---

### Notifications

Verify:

- Push Notifications
- Email Notifications
- In-App Notifications

Reference

flows/notifications.md

---

## Cross-Platform Validation

For every feature, AI agents should verify:

- Feature parity across Web, Android, and iOS.
- Platform-specific UI differences.
- Platform-specific limitations.
- Consistent business logic.
- Consistent API behavior.

---

## Accessibility Validation

Where applicable, verify:

- Readable text
- Proper button labels
- Focus behavior
- Keyboard navigation (Web)
- Screen reader compatibility

---

## AI Agent Instructions

When generating frontend automation:

- Validate complete user journeys instead of isolated screens.
- Follow documented business rules.
- Verify positive, negative, and edge-case scenarios.
- Capture screenshots for failures.
- Report console errors, API failures, and UI inconsistencies.
- Do not assume feature behavior that is not documented.

## Regression Priority

### High Priority

- Authentication
- Login
- Registration
- KYC
- Wallet
- Payments
- Contest Join
- Draft
- Pick'em Submission

### Medium Priority

- Rankings
- Notifications
- Profile
- Promotions

### Low Priority

- Static Content
- Help Pages
- FAQs

# 9. API QA Guidelines

## Overview

The Drafters platform relies on REST APIs to support Web, Android, iOS, and Admin Portal functionality. AI agents should validate API behavior against documented business requirements and ensure consistent responses across all supported platforms.

Detailed endpoint documentation should be maintained under the `api/` directory.

---

## API Validation Standards

AI agents should validate the following for every API unless explicitly documented otherwise.

### Request Validation

- Verify required request parameters.
- Verify optional request parameters.
- Verify request headers.
- Verify authentication token requirements.
- Verify supported HTTP methods.
- Verify request payload format.

---

### Response Validation

Verify:

- Correct HTTP status code.
- Response follows the documented schema.
- Required fields are present.
- Data types are correct.
- Response values match business expectations.
- No unexpected or null values are returned.

---

### Authentication & Authorization

Verify:

- Protected APIs require authentication.
- Invalid or expired tokens are rejected.
- Unauthorized users cannot access restricted APIs.
- Role-based access control is enforced.

---

### Input Validation

Verify handling of:

- Missing required fields.
- Invalid data types.
- Empty values.
- Boundary values.
- Invalid formats.
- Duplicate requests.
- Malicious input where applicable.

---

### Error Handling

Verify:

- Appropriate HTTP status codes.
- User-friendly error messages.
- No internal server implementation details are exposed.
- Stack traces are never returned.
- Error responses follow a consistent format.

---

### Performance Validation

Verify:

- API response time meets project performance expectations.
- No unnecessary delays.
- APIs remain responsive under normal usage.
- Timeouts are handled correctly.

---

### Data Validation

Verify:

- Database updates are reflected correctly.
- Response data matches stored data.
- Calculated values are accurate.
- Transactions are committed correctly.
- No duplicate records are created.

---

### Security Validation

Verify:

- Sensitive information is never exposed.
- Passwords and secrets are never returned.
- Tokens are securely handled.
- HTTPS is used where applicable.
- Authorization rules are enforced.

---

## API Categories

The Drafters platform includes APIs for:

- Authentication
- Registration
- User Profile
- KYC
- Wallet
- Payments
- Contest Management
- Draft
- Pick'em
- Rankings
- Notifications
- Responsible Gaming
- Admin Portal

Detailed documentation for each category should be maintained in the `api/` directory.

---

## Common HTTP Status Codes

| Status Code | Meaning |
|-------------|---------|
| 200 | Success |
| 201 | Resource Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Resource Not Found |
| 409 | Conflict |
| 422 | Validation Error |
| 500 | Internal Server Error |

---

## AI Agent Instructions

When validating APIs:

1. Verify request and response structures.
2. Validate business rules.
3. Check authentication and authorization.
4. Verify database consistency where applicable.
5. Report failed API requests with request and response details.
6. Never expose secrets or authentication credentials in reports.
7. Follow the documented API specification before generating automation.

## API Regression Priority

### High Priority

- Authentication APIs
- Registration APIs
- Wallet APIs
- Payment APIs
- Contest Join APIs
- Draft APIs

### Medium Priority

- Rankings APIs
- Notifications APIs
- Profile APIs

### Low Priority

- Static Configuration APIs
- Content APIs

# 11. Logging Requirements

## Overview

Logs are essential for identifying, diagnosing, and resolving application issues. AI agents should inspect relevant logs during test execution, automation failures, API validation, and defect analysis.

Whenever a test fails, AI agents should collect and analyze the appropriate logs before reporting the issue.

---

## Browser Console Logs (Web)

AI agents should verify:

- No JavaScript errors.
- No uncaught exceptions.
- No deprecated API warnings affecting functionality.
- No failed resource loading.
- No unexpected console errors during user interactions.

Report:

- JavaScript Exceptions
- Console Errors
- Failed Resource Loading
- Unexpected Warnings affecting application behavior

Ignore:

- Browser extension warnings
- Known third-party library warnings (if documented)
- Non-impacting informational messages

---

## Network Logs

AI agents should inspect:

- Failed API requests
- Incorrect HTTP status codes
- Request payload validation
- Response payload validation
- API response time
- Authentication failures

Report:

- 4xx Errors (Unexpected)
- 5xx Errors
- Timeout Errors
- API Contract Violations

---

## Android Logs (Logcat)

AI agents should verify:

- No application crashes
- No ANR (Application Not Responding)
- No uncaught exceptions
- No repeated runtime errors

Report:

- Fatal Exceptions
- Application Crashes
- Memory Issues
- Unexpected Errors

Ignore:

- Known SDK warnings
- Debug logs
- Informational logs

---

## iOS Logs

AI agents should verify:

- No application crashes
- No runtime exceptions
- No unexpected system errors

Report:

- Crash Logs
- Fatal Exceptions
- Critical Runtime Errors

Ignore:

- Apple framework informational logs
- Known simulator warnings (if applicable)

---

## Backend Logs

Verify:

- API execution
- Business validation failures
- Authentication failures
- Database exceptions
- Payment processing errors
- Integration failures

Report:

- Unhandled Exceptions
- Database Errors
- Payment Gateway Errors
- Internal Server Errors

---

## Database Logs

Verify:

- Query execution failures
- Connection issues
- Transaction failures
- Deadlocks
- Data consistency errors

---

## Third-Party Integration Logs

Verify integrations including:

- Finix Payment Gateway
- PayPal
- KYC Provider
- Push Notification Services
- Email Services

Report:

- Authentication failures
- API failures
- Timeout errors
- Invalid responses
- Service unavailable errors

---

## Performance Logs

Verify:

- Slow API responses
- Long page load times
- High memory usage
- Excessive CPU utilization
- Network latency

---

## AI Agent Instructions

When investigating failures:

1. Capture browser console logs (Web).
2. Capture network logs.
3. Capture Android Logcat or iOS device logs.
4. Capture backend logs if available.
5. Capture relevant API request and response details.
6. Attach logs to defect reports whenever possible.
7. Distinguish between expected warnings and actual defects.
8. Never ignore fatal exceptions or server errors.

---

## Logging Best Practices

- Always include timestamps in reports.
- Record the environment (Development, Staging, Production Reference).
- Include user role and platform information.
- Capture reproducible log evidence.
- Avoid exposing sensitive information such as passwords, API keys, or authentication tokens in logs.

# 12. Performance Expectations

## Overview

The Drafters platform should provide a fast, responsive, and reliable experience across Web, Android, iOS, and the Admin Portal.

AI agents should evaluate performance during functional testing, automation execution, and regression testing. Performance issues that negatively impact the user experience should be reported.

---

## General Performance Guidelines

AI agents should verify:

- Pages load within acceptable time.
- APIs respond within expected limits.
- UI interactions remain responsive.
- Loading indicators appear and disappear correctly.
- No application freezes or crashes occur.
- No excessive memory or CPU usage is observed.

---

## Web Performance

Verify:

- Homepage loads successfully.
- Lobby and Contest pages load efficiently.
- Navigation between pages is smooth.
- Images and assets load completely.
- No unnecessary page refreshes occur.

Expected Results

- Fast page rendering.
- Smooth scrolling.
- No browser freezing.
- No layout shifts after loading.

---

## Mobile Performance (Android & iOS)

Verify:

- Application launches successfully.
- Screens load without excessive delay.
- Navigation between screens is smooth.
- No UI lag during user interactions.
- Animations remain responsive.

Expected Results

- Stable application performance.
- No ANR (Android Not Responding).
- No application crashes.
- Smooth transitions between screens.

---

## API Performance

Verify:

- API responses are received within acceptable response times.
- No timeout errors.
- Retry mechanisms work correctly where applicable.

Expected Results

- APIs respond consistently.
- No unnecessary retries.
- No excessive latency.

---

## Authentication Performance

Verify:

- Login completes successfully.
- Registration completes within acceptable time.
- Password reset requests process correctly.
- Session validation is responsive.

---

## Wallet & Payment Performance

Verify:

- Wallet balance loads correctly.
- Deposit flow completes without unnecessary delays.
- Payment processing remains responsive.
- Transaction history loads successfully.

Expected Results

- No duplicate requests.
- No loading loops.
- Accurate transaction updates.

---

## Contest & Draft Performance

Verify:

- Contest Lobby loads correctly.
- Contest Details open quickly.
- Draft Room loads before draft begins.
- Player selection responds immediately.
- Countdown timers remain synchronized.

Expected Results

- No delayed player selections.
- No missed draft actions.
- Real-time updates function correctly.

---

## Rankings & Leaderboards

Verify:

- Rankings load successfully.
- Sorting and filtering remain responsive.
- Leaderboards refresh correctly.

---

## Notifications

Verify:

- Push notifications are delivered promptly.
- Notification screens load correctly.
- Notification status updates accurately.

---

## Performance Monitoring

Where available, AI agents should review:

- Browser Developer Tools
- Network Timing
- Mobile Performance Metrics
- Application Logs
- Backend Monitoring Tools

---

## AI Agent Instructions

When evaluating performance:

1. Measure response times where possible.
2. Report noticeable performance degradation.
3. Compare current performance against previous releases.
4. Capture screenshots or logs for performance issues.
5. Distinguish between network-related issues and application performance issues.
6. Escalate performance regressions affecting user experience.

---

## Performance Best Practices

- Avoid unnecessary page reloads.
- Minimize repeated API calls.
- Ensure efficient resource loading.
- Validate loading indicators.
- Verify application responsiveness across supported platforms.
- Report performance regressions during regression testing.
