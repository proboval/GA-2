Saveliy Chertkov
### **2. Governance Policy**
#### 2.1 Roles and Responsibilities

| Role               | Responsibilities                                |
| ------------------ | ----------------------------------------------- |
| Core Mainteiners   | Final approval of changes, high-level structure |
| Technical writers  | Drafting, editing, ensuring clarity             |
| QA Engineers       | Testing code examples, verifying workflows      |
| Community Managers | Handling feedback, deprecation announcements    |
#### 2.2 Review Cycle

| Stage                                | Frequency    | Participants                          |
| ------------------------------------ | ------------ | ------------------------------------- |
| Minor Updates (typos, brooken links) | Ad-hoc       | Tech Writers                          |
| Major Updates                        | Quarterly    | Core Team, Tech Writers, QA Engineers |
| Checking for outdated content        | Semiannually | Community Managers                    |
#### 2.3 Approval Workflow
All changes follow:
`Draft -> Review -> Publish`
1. **Draft**
	Create a new branch in the `docs/` branch containing the changes 
2. **Review** 
	*Required for new features*
	* Technical review: verify accuracy
	* Editorial review: check clarity/style
3. **Publish**
	Merged to `main` with version tag
#### 2.4 Archival Rules
* **Active version**: Last 2 major releases (e.g., `pytest 7.x`, `pytest 8.x`)
* **Deprecated Content**: Moved to `/archive` (separate directory in the repository, stored in the `main` branch)
**Exceptions**:	
- Community-contributed plugins archived after 2 years of inactivity
#### 2.5 Compliance & Metrics
- **Audits**: Quarterly check for outdated content 
- **Feedback**: Monthly survey (rated 1–5 on usefulness).
- **SLAs**:
    - Crucial fixes (broken code samples): 48 hours
    - Major updates: 2-week review window