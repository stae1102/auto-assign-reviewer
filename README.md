# auto-assign-reviewer-study

> 효율적인 코드 리뷰문화 정착을 위한 레포지터리입니다.

## 템플릿 적용

`.github/pull_request_template.md` 를 통해 PR시 빠르고 규칙적으로 PR을 남길 수 있습니다.

## 리뷰어 자동 등록 액션

### Auto-assign 액션

https://github.com/apps/auto-assign

- 해당 액션을 통해 그룹 및 개인으로 리뷰어를 등록할 수 있습니다.

```yaml
# Reviewer를 PR에 추가하고자 할 때 true로 설정하세요.
addReviewers: true

# Assignee를 PR에 추가하고자 할 때 true로 설정하세요.
addAssignees: false

# PR에 추가된 reviewer의 수
# 0으로 설정해 모든 reviewer를 추가할 수 있습니다 (기본값: 0)
numberOfReviewers: 1

# PR에 추가된 assignee의 수
# 0으로 설정해 모든 assignee를 추가할 수 있습니다.
# 설정되어 있지 않은 경우 numberOfReviewers를 사용합니다.
# numberOfAssignees: 2

# Set to true to add reviewers from different groups to pull requests
# true로 설정하여 다른 그룹으로부터 PR에 reviewer를 추가할 수 있습니다.
useReviewGroups: true

# Reviewer를 그룹으로 나눌 수 있습니다.
# GitHub username을 사용합니다.
reviewGroups:
  groupA:
    - reviewerA
    - reviewerB
    - reviewerC
  groupB:
    - reviewerD
    - reviewerE
    - reviewerF

# true로 설정하여 다른 그룹으로부터 PR에 assignee를 추가할 수 있습니다.
useAssigneeGroups: false

# Assignee를 그룹으로 나눌 수 있습니다.
# GitHub username을 사용합니다.
# assigneeGroups:
#   groupA:
#     - assigneeA
#     - assigneeB
#     - assigneeC
#   groupB:
#     - assigneeD
#     - assigneeE
#     - assigneeF

# 특정 키워드가 포함돼 있을 때 Reviewer를 추가하지 않도록 하는 키워드입니다.
# skipKeywords:
#   - wip

# Author로 설정하여 PR 생성자를 assignee로 설정합니다.
addAssignees: author
```

### CODEOWNER

https://docs.github.com/ko/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners

- 액션은 아니지만, 코드 리뷰어를 개인/팀 단위로 빠르게 지정할 수 있습니다.
- Thanks for [혜성님](https://github.com/hyesungoh)
