---
tags:
  - Audit
date: 31-03-2025
---

Saveliy Chertkov
[PyTest Documentation](https://app.readthedocs.org/projects/pytest/downloads/pdf/latest/)
### **1. Audit Documentation**
#### 1.1 Outdate information:
1. **The pytest-pep8 plugin**
	The pytest-pep8 plugin is already deprecated and has been replaced by the pytest-flake8 plugin, but it is found in the plugin list.
2. **Python 2.7**
	The documentation leaves out references and examples to Python 2.7, which is no longer supported [p. 451].
#### 1.2 Missing information:
1. **Fixtures: `yield` vs `addfinalizer`** [pp. 29 - 31]
	There are both options in the documentation, but `yield` has become a standard and `addfinalizer` is hardly used. The documentation states that `yield` is preferred for use, but for new users, it is better to add why `yield` is recommended.
2. **Parametrize (`@pytest.mark.parametrize`) with dynamic data**
	There are no clear examples of how to generate parameters dynamically (e.g., from a file or API).
3. **Mocking (e.g. `unittest.mock` vs `pytest-mock`)**
	It's not always clear when to use inbuilt mocs and when to use outside plugins.
4. Asynchronous testing (`pytest-asyncio`)
	Clarification is required for asyncio test examples.
#### 1.3 Update schedule and assign owners
##### Phase 1: Quick fixes (31.03.2025 - 18.04.2025)

| Task                                                                             | Owner          | Start date | End Date   |
| -------------------------------------------------------------------------------- | -------------- | ---------- | ---------- |
| Remove references to `Python 2.x`                                                | @tech_writer   | 31.03.2025 | 7.04.2025  |
| Update the list of plugins (remove `pytest-pep8`), analyze the remaining plugins | @community_mng | 7.04.2025  | 18.04.2025 |

##### Phase 2: Improve Documentation (21.04.205 - 7.05.2025)

| Task                                                             | Owner                           | Start date | End Date  |
| ---------------------------------------------------------------- | ------------------------------- | ---------- | --------- |
| Add dynamic parametrize <br>examples (`pytest.mark.parametrize`) | @qa-engineer and @tech_writer_1 | 21.04.2025 | 2.05.2025 |
| Add a section on asynchronous <br>tests (`pytest-asyncio`)       | @core_dev and @tech_writer_1    | 21.04.2025 | 7.05.2025 |
| Improve mock documentation (`unittest.mock` vs `pytest-mock`)    | @tech_writer_2                  | 21.04.2025 | 5.05.2025 |
#### 1.4 Track Changes
1. **GitHub (main storage)**
	* Branch `docs/update-2025` for all changes 
	* Separate branch for every changes
	* Version labels (e.g., pytest-8.3+ in the description of changes).
2. **Pre-merge checklist**
	* All examples work on pytest 8.x.
	* No broken links (check with pytest --dead-links).
	* Conformity to style (readability, terminology).
