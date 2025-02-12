---
title: Permissões necessárias para os aplicativos GitHub
intro: 'Você pode encontrar as permissões necessárias para cada ponto de extremidade compatível com {% data variables.product.prodname_github_app %}.'
redirect_from:
  - /v3/apps/permissions
  - /rest/reference/permissions-required-for-github-apps
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - API
miniTocMaxHeadingLevel: 3
shortTitle: GitHub App permissions
ms.openlocfilehash: 9b0344213069be96e86029adef157dba032f9de6
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/05/2022
ms.locfileid: '147560783'
---
### Sobre as permissões de {% data variables.product.prodname_github_app %}

{% data variables.product.prodname_github_apps %} são criadas com um conjunto de permissões. As permissões definem quais recursos o {% data variables.product.prodname_github_app %} pode acessar através da API. Para obter mais informações, confira "[Como configurar permissões para Aplicativos do GitHub](/apps/building-github-apps/setting-permissions-for-github-apps/)".

### Permissões de metadados

Os Aplicativos do GitHub têm a permissão de metadados `Read-only` por padrão. A permissão de metadados fornece acesso a uma coleção de pontos de extremidade somente leitura com metadados para vários recursos. Esses pontos de extremidade não vazam informações privadas sobre repositórios.

{% data reusables.apps.metadata-permissions %}

- [`GET /`](/rest#root-endpoint)
- [`GET /codes_of_conduct`](/rest/reference/codes-of-conduct#get-all-codes-of-conduct)
- [`GET /codes_of_conduct/:key`](/rest/reference/codes-of-conduct#get-a-code-of-conduct)
- [`GET /emojis`](/rest/reference/emojis#emojis)
- [`GET /feeds`](/rest/reference/activity#get-feeds)
- [`GET /licenses`](/rest/reference/licenses#get-all-commonly-used-licenses)
- [`GET /licenses/:key`](/rest/reference/licenses#get-a-license)
- [`POST /markdown`](/rest/reference/markdown#render-a-markdown-document)
- [`POST /markdown/raw`](/rest/reference/markdown#render-a-markdown-document-in-raw-mode)
- [`GET /meta`](/rest/reference/meta#meta)
- [`GET /organizations`](/rest/reference/orgs#list-organizations)
- [`GET /orgs/:org`](/rest/reference/orgs#get-an-organization)
- [`GET /orgs/:org/projects`](/rest/reference/projects#list-organization-projects)
- [`GET /orgs/:org/repos`](/rest/reference/repos#list-organization-repositories)
- [`GET /rate_limit`](/rest/reference/rate-limit#get-rate-limit-status-for-the-authenticated-user)
- [`GET /repos/:owner/:repo`](/rest/reference/repos#get-a-repository) {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/community/profile`](/rest/reference/repository-metrics#get-community-profile-metrics) {% endif -%}
- [`GET /repos/:owner/:repo/contributors`](/rest/reference/repos#list-repository-contributors)
- [`GET /repos/:owner/:repo/forks`](/rest/reference/repos#list-forks)
- [`GET /repos/:owner/:repo/languages`](/rest/reference/repos#list-repository-languages)
- [`GET /repos/:owner/:repo/license`](/rest/reference/licenses#get-the-license-for-a-repository)
- [`GET /repos/:owner/:repo/stargazers`](/rest/reference/activity#list-stargazers)
- [`GET /repos/:owner/:repo/stats/code_frequency`](/rest/reference/repository-metrics#get-the-weekly-commit-activity)
- [`GET /repos/:owner/:repo/stats/commit_activity`](/rest/reference/repository-metrics#get-the-last-year-of-commit-activity)
- [`GET /repos/:owner/:repo/stats/contributors`](/rest/reference/repository-metrics#get-all-contributor-commit-activity)
- [`GET /repos/:owner/:repo/stats/participation`](/rest/reference/repository-metrics#get-the-weekly-commit-count)
- [`GET /repos/:owner/:repo/stats/punch_card`](/rest/reference/repository-metrics#get-the-hourly-commit-count-for-each-day)
- [`GET /repos/:owner/:repo/subscribers`](/rest/reference/activity#list-watchers)
- [`GET /repos/:owner/:repo/tags`](/rest/reference/repos#list-repository-tags)
- [`GET /repos/:owner/:repo/topics`](/rest/reference/repos#get-all-repository-topics)
- [`GET /repositories`](/rest/reference/repos#list-public-repositories)
- [`GET /user/repos`](/rest/reference/repos#list-repositories-for-the-authenticated-user)
- [`GET /user/starred`](/rest/reference/activity#list-repositories-starred-by-a-user)
- [`GET /user/subscriptions`](/rest/reference/activity#list-repositories-watched-by-a-user)
- [`GET /users`](/rest/reference/users#list-users)
- [`GET /users/:username`](/rest/reference/users#get-a-user)
- [`GET /users/:username/followers`](/rest/reference/users#list-followers-of-a-user)
- [`GET /users/:username/following`](/rest/reference/users#list-the-people-a-user-follows)
- [`GET /users/:username/following/:target_user`](/rest/reference/users#check-if-a-user-follows-another-user)
- [`GET /users/:username/gpg_keys`](/rest/reference/users#list-gpg-keys-for-a-user)
- [`GET /users/:username/orgs`](/rest/reference/orgs#list-organizations-for-a-user)
- [`GET /users/:username/received_events`](/rest/reference/activity#list-events-received-by-the-authenticated-user)
- [`GET /users/:username/received_events/public`](/rest/reference/activity#list-public-events-received-by-a-user)
- [`GET /users/:username/repos`](/rest/reference/repos#list-repositories-for-a-user)
- [`GET /users/:username/subscriptions`](/rest/reference/activity#list-repositories-watched-by-a-user)

_Colaboradores_
- [`GET /repos/:owner/:repo/collaborators`](/rest/reference/collaborators#list-repository-collaborators)
- [`GET /repos/:owner/:repo/collaborators/:username`](/rest/reference/collaborators#check-if-a-user-is-a-repository-collaborator)

_Comentários sobre um commit_
- [`GET /repos/:owner/:repo/comments`](/rest/reference/commits#list-commit-comments-for-a-repository)
- [`GET /repos/:owner/:repo/comments/:comment_id`](/rest/reference/commits#get-a-commit-comment)
- [`GET /repos/:owner/:repo/comments/:comment_id/reactions`](/rest/reference/reactions#list-reactions-for-a-commit-comment)
- [`GET /repos/:owner/:repo/commits/:sha/comments`](/rest/reference/commits#list-commit-comments)

_Eventos_
- [`GET /events`](/rest/reference/activity#list-public-events)
- [`GET /networks/:owner/:repo/events`](/rest/reference/activity#list-public-events-for-a-network-of-repositories)
- [`GET /orgs/:org/events`](/rest/reference/activity#list-public-organization-events)
- [`GET /repos/:owner/:repo/events`](/rest/reference/activity#list-repository-events)
- [`GET /repos/:owner/:repo/events/issues`](/rest/reference/issues#list-issue-events-for-a-repository)
- [`GET /users/:username/events`](/rest/reference/activity#list-events-for-the-authenticated-user)
- [`GET /users/:username/events/public`](/rest/reference/activity#list-public-events-for-a-user)

_Git_
- [`GET /gitignore/templates`](/rest/reference/gitignore#get-all-gitignore-templates)
- [`GET /gitignore/templates/:key`](/rest/reference/gitignore#get-a-gitignore-template)

_Chaves_
- [`GET /users/:username/keys`](/rest/reference/users#list-public-keys-for-a-user)

_Membros da organização_
- [`GET /orgs/:org/members`](/rest/reference/orgs#list-organization-members)
- [`GET /orgs/:org/members/:username`](/rest/reference/orgs#check-organization-membership-for-a-user)
- [`GET /orgs/:org/public_members`](/rest/reference/orgs#list-public-organization-members)
- [`GET /orgs/:org/public_members/:username`](/rest/reference/orgs#check-public-organization-membership-for-a-user)

_Pesquisar_
- [`GET /search/code`](/rest/reference/search#search-code)
- [`GET /search/commits`](/rest/reference/search#search-commits)
- [`GET /search/issues`](/rest/reference/search#search-issues-and-pull-requests)
- [`GET /search/labels`](/rest/reference/search#search-labels)
- [`GET /search/repositories`](/rest/reference/search#search-repositories)
- [`GET /search/topics`](/rest/reference/search#search-topics)
- [`GET /search/users`](/rest/reference/search#search-users)

{% ifversion fpt or ghes or ghec %}
### Permissão em "ações"

- [`GET /repos/:owner/:repo/actions/artifacts`](/rest/reference/actions#list-artifacts-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/actions/artifacts/:artifact_id`](/rest/reference/actions#get-an-artifact) (:leitura)
- [`DELETE /repos/:owner/:repo/actions/artifacts/:artifact_id`](/rest/reference/actions#delete-an-artifact) (:gravação)
- [`GET /repos/:owner/:repo/actions/artifacts/:artifact_id/zip`](/rest/reference/actions#download-an-artifact) (:leitura) {% ifversion actions-cache-management -%}
- [`GET /repos/:owner/:repo/actions/cache/usage`](/rest/reference/actions#get-github-actions-cache-usage-for-a-repository) (:leitura) {% endif -%}
- [`GET /repos/:owner/:repo/actions/jobs/:job_id`](/rest/reference/actions#get-a-job-for-a-workflow-run) (:leitura)
- [`GET /repos/:owner/:repo/actions/jobs/:job_id/logs`](/rest/reference/actions#download-job-logs-for-a-workflow-run) (:leitura)
- [`GET /repos/:owner/:repo/actions/runs`](/rest/reference/actions#list-workflow-runs-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/actions/runs/:run_id`](/rest/reference/actions#get-a-workflow-run) (:leitura) {% ifversion fpt or ghec -%}
- [`POST /repos/:owner/:repo/actions/runs/:run_id/approve`](/rest/reference/actions#approve-a-workflow-run-for-a-fork-pull-request) (:gravação) {% endif -%}
- [`GET /repos/:owner/:repo/actions/runs/:run_id/artifacts`](/rest/reference/actions#list-workflow-run-artifacts) (:leitura)
- [`POST /repos/:owner/:repo/actions/runs/:run_id/cancel`](/rest/reference/actions#cancel-a-workflow-run) (:gravação)
- [`GET /repos/:owner/:repo/actions/runs/:run_id/jobs`](/rest/reference/actions#list-jobs-for-a-workflow-run) (:leitura)
- [`GET /repos/:owner/:repo/actions/runs/:run_id/logs`](/rest/reference/actions#download-workflow-run-logs) (:leitura)
- [`DELETE /repos/:owner/:repo/actions/runs/:run_id/logs`](/rest/reference/actions#delete-workflow-run-logs) (:gravação)
- [`POST /repos/:owner/:repo/actions/runs/:run_id/rerun`](/rest/reference/actions#re-run-a-workflow) (:gravação)
- [`GET /repos/:owner/:repo/actions/workflows`](/rest/reference/actions#list-repository-workflows) (:leitura)
- [`GET /repos/:owner/:repo/actions/workflows/:workflow_id`](/rest/reference/actions#get-a-workflow) (:leitura)
- [`GET /repos/:owner/:repo/actions/workflows/:workflow_id/runs`](/rest/reference/actions#list-workflow-runs) (:leitura) {% endif %}

### Permissão em "administração"

- [`POST /orgs/:org/repos`](/rest/reference/repos#create-an-organization-repository) (:gravação)
- [`PATCH /repos/:owner/:repo`](/rest/reference/repos#update-a-repository) (:gravação)
- [`DELETE /repos/:owner/:repo`](/rest/reference/repos#delete-a-repository) (:gravação)
- [`GET /repos/:owner/:repo/actions/runners/downloads`](/rest/reference/actions#list-runner-applications-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/actions/runners`](/rest/reference/actions#list-self-hosted-runners-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/actions/runners/:runner_id`](/rest/reference/actions#get-a-self-hosted-runner-for-a-repository) (:leitura)
- [`DELETE /repos/:owner/:repo/actions/runners/:runner_id`](/rest/reference/actions#delete-a-self-hosted-runner-from-a-repository) (:gravação)
- [`GET /repos/:owner/:repo/actions/runners/:runner_id/labels`](/rest/reference/actions#list-labels-for-a-self-hosted-runner-for-a-repository) (:leitura)
- [`POST /repos/:owner/:repo/actions/runners/:runner_id/labels`](/rest/reference/actions#add-custom-labels-to-a-self-hosted-runner-for-a-repository) (:gravação)
- [`PUT /repos/:owner/:repo/actions/runners/:runner_id/labels`](/rest/reference/actions#set-custom-labels-for-a-self-hosted-runner-for-a-repository) (:gravação)
- [`DELETE /repos/:owner/:repo/actions/runners/:runner_id/labels`](/rest/reference/actions#remove-all-custom-labels-from-a-self-hosted-runner-for-a-repository) (:gravação)
- [`DELETE /repos/:owner/:repo/actions/runners/:runner_id/labels/:name`](/rest/reference/actions#remove-a-custom-label-from-a-self-hosted-runner-for-a-repository) (:gravação) {% ifversion fpt or ghec or ghes -%}
- [`POST /repos/:owner/:repo/actions/runners/registration-token`](/rest/reference/actions#create-a-registration-token-for-a-repository) (:gravação)
- [`POST /repos/:owner/:repo/actions/runners/remove-token`](/rest/reference/actions#create-a-remove-token-for-a-repository) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`PUT /repos/:owner/:repo/automated-security-fixes`](/rest/reference/repos#enable-automated-security-fixes) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /repos/:owner/:repo/automated-security-fixes`](/rest/reference/repos#disable-automated-security-fixes) (:gravação) {% endif -%}
- [`POST /repos/:owner/:repo/forks`](/rest/reference/repos#create-a-fork) (:gravação) {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/interaction-limits`](/rest/reference/interactions#get-interaction-restrictions-for-a-repository) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`PUT /repos/:owner/:repo/interaction-limits`](/rest/reference/interactions#set-interaction-restrictions-for-a-repository) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /repos/:owner/:repo/interaction-limits`](/rest/reference/interactions#remove-interaction-restrictions-for-a-repository) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/pages/health`](/rest/reference/pages#get-a-dns-health-check-for-github-pages) (:gravação) {% endif -%} {% ifversion ghes > 3.3 -%}
- [`GET /repos/:owner/:repo/replicas/caches`](/rest/reference/repos#list-repository-cache-replication-status) (:leitura) {% endif -%}
- [`PUT /repos/:owner/:repo/topics`](/rest/reference/repos#replace-all-repository-topics) (:gravação)
- [`POST /repos/:owner/:repo/transfer`](/rest/reference/repos#transfer-a-repository) (:gravação) {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/vulnerability-alerts`](/rest/reference/repos#enable-vulnerability-alerts) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`PUT /repos/:owner/:repo/vulnerability-alerts`](/rest/reference/repos#enable-vulnerability-alerts) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /repos/:owner/:repo/vulnerability-alerts`](/rest/reference/repos#disable-vulnerability-alerts) (:gravação) {% endif -%}
- [`PATCH /user/repository_invitations/:invitation_id`](/rest/reference/collaborators#accept-a-repository-invitation) (:gravação)
- [`DELETE /user/repository_invitations/:invitation_id`](/rest/reference/collaborators#decline-a-repository-invitation) (:gravação)

_Branches_
- [`GET /repos/:owner/:repo/branches/:branch/protection`](/rest/reference/branches#get-branch-protection) (:leitura)
- [`PUT /repos/:owner/:repo/branches/:branch/protection`](/rest/reference/branches#update-branch-protection) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection`](/rest/reference/branches#delete-branch-protection) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/enforce_admins`](/rest/reference/branches#get-admin-branch-protection) (:leitura)
- [`POST /repos/:owner/:repo/branches/:branch/protection/enforce_admins`](/rest/reference/branches#set-admin-branch-protection) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/enforce_admins`](/rest/reference/branches#delete-admin-branch-protection) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/required_pull_request_reviews`](/rest/reference/branches#get-pull-request-review-protection) (:leitura)
- [`PATCH /repos/:owner/:repo/branches/:branch/protection/required_pull_request_reviews`](/rest/reference/branches#update-pull-request-review-protection) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/required_pull_request_reviews`](/rest/reference/branches#delete-pull-request-review-protection) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/required_signatures`](/rest/reference/branches#get-commit-signature-protection) (:leitura)
- [`POST /repos/:owner/:repo/branches/:branch/protection/required_signatures`](/rest/reference/branches#create-commit-signature-protection) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/required_signatures`](/rest/reference/branches#delete-commit-signature-protection) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/required_status_checks`](/rest/reference/branches#get-status-checks-protection) (:leitura)
- [`PATCH /repos/:owner/:repo/branches/:branch/protection/required_status_checks`](/rest/reference/branches#update-status-check-protection) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/required_status_checks`](/rest/reference/branches#remove-status-check-protection) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/required_status_checks/contexts`](/rest/reference/branches#get-all-status-check-contexts) (:leitura)
- [`POST /repos/:owner/:repo/branches/:branch/protection/required_status_checks/contexts`](/rest/reference/branches#add-status-check-contexts) (:gravação)
- [`PUT /repos/:owner/:repo/branches/:branch/protection/required_status_checks/contexts`](/rest/reference/branches#set-status-check-contexts) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/required_status_checks/contexts`](/rest/reference/branches#remove-status-check-contexts) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/restrictions`](/rest/reference/branches#get-access-restrictions) (:leitura)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/restrictions`](/rest/reference/branches#delete-access-restrictions) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/restrictions/teams`](/rest/reference/repos#list-teams-with-access-to-the-protected-branch) (:leitura)
- [`POST /repos/:owner/:repo/branches/:branch/protection/restrictions/teams`](/rest/reference/branches#add-team-access-restrictions) (:gravação)
- [`PUT /repos/:owner/:repo/branches/:branch/protection/restrictions/teams`](/rest/reference/branches#set-team-access-restrictions) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/restrictions/teams`](/rest/reference/branches#remove-team-access-restrictions) (:gravação)
- [`GET /repos/:owner/:repo/branches/:branch/protection/restrictions/users`](/rest/reference/repos#list-users-with-access-to-the-protected-branch) (:leitura)
- [`POST /repos/:owner/:repo/branches/:branch/protection/restrictions/users`](/rest/reference/branches#add-user-access-restrictions) (:gravação)
- [`PUT /repos/:owner/:repo/branches/:branch/protection/restrictions/users`](/rest/reference/branches#set-user-access-restrictions) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/restrictions/users`](/rest/reference/branches#remove-user-access-restrictions) (:gravação)
- [`POST /repos/:owner/:repo/branches/:branch/rename`](/rest/reference/branches#rename-a-branch) (:gravação)

_Colaboradores_
- [`PUT /repos/:owner/:repo/collaborators/:username`](/rest/reference/collaborators#add-a-repository-collaborator) (:gravação)
- [`DELETE /repos/:owner/:repo/collaborators/:username`](/rest/reference/collaborators#remove-a-repository-collaborator) (:gravação)

_Convites_
- [`GET /repos/:owner/:repo/invitations`](/rest/reference/collaborators#list-repository-invitations) (:leitura)
- [`PATCH /repos/:owner/:repo/invitations/:invitation_id`](/rest/reference/collaborators#update-a-repository-invitation) (:gravação)
- [`DELETE /repos/:owner/:repo/invitations/:invitation_id`](/rest/reference/collaborators#delete-a-repository-invitation) (:gravação)

_Chaves_
- [`GET /repos/:owner/:repo/keys`](/rest/reference/deployments#list-deploy-keys) (:leitura)
- [`POST /repos/:owner/:repo/keys`](/rest/reference/deployments#create-a-deploy-key) (:gravação)
- [`GET /repos/:owner/:repo/keys/:key_id`](/rest/reference/deployments#get-a-deploy-key) (:leitura)
- [`DELETE /repos/:owner/:repo/keys/:key_id`](/rest/reference/deployments#delete-a-deploy-key) (:gravação)

_Teams_
- [`GET /repos/:owner/:repo/teams`](/rest/reference/repos#list-repository-teams) (:leitura)
- [`PUT /teams/:team_id/repos/:owner/:repo`](/rest/reference/teams#add-or-update-team-repository-permissions) (:gravação)
- [`DELETE /teams/:team_id/repos/:owner/:repo`](/rest/reference/teams#remove-a-repository-from-a-team) (:gravação)

{% ifversion fpt or ghec %} _Tráfego_
- [`GET /repos/:owner/:repo/traffic/clones`](/rest/reference/repository-metrics#get-repository-clones) (:leitura)
- [`GET /repos/:owner/:repo/traffic/popular/paths`](/rest/reference/repository-metrics#get-top-referral-paths) (:leitura)
- [`GET /repos/:owner/:repo/traffic/popular/referrers`](/rest/reference/repository-metrics#get-top-referral-sources) (:leitura)
- [`GET /repos/:owner/:repo/traffic/views`](/rest/reference/repository-metrics#get-page-views) (:leitura) {% endif %}

{% ifversion fpt or ghec %}
### Permissão em "bloqueio"

- [`GET /user/blocks`](/rest/reference/users#list-users-blocked-by-the-authenticated-user) (:leitura)
- [`GET /user/blocks/:username`](/rest/reference/users#check-if-a-user-is-blocked-by-the-authenticated-user) (:leitura)
- [`PUT /user/blocks/:username`](/rest/reference/users#block-a-user) (:gravação)
- [`DELETE /user/blocks/:username`](/rest/reference/users#unblock-a-user) (:gravação) {% endif %}

### Permissão em "verificações"

- [`POST /repos/:owner/:repo/check-runs`](/rest/reference/checks#create-a-check-run) (:gravação)
- [`GET /repos/:owner/:repo/check-runs/:check_run_id`](/rest/reference/checks#get-a-check-run) (:leitura)
- [`PATCH /repos/:owner/:repo/check-runs/:check_run_id`](/rest/reference/checks#update-a-check-run) (:gravação)
- [`GET /repos/:owner/:repo/check-runs/:check_run_id/annotations`](/rest/reference/checks#list-check-run-annotations) (:leitura)
- [`POST /repos/:owner/:repo/check-suites`](/rest/reference/checks#create-a-check-suite) (:gravação)
- [`GET /repos/:owner/:repo/check-suites/:check_suite_id`](/rest/reference/checks#get-a-check-suite) (:leitura)
- [`GET /repos/:owner/:repo/check-suites/:check_suite_id/check-runs`](/rest/reference/checks#list-check-runs-in-a-check-suite) (:leitura)
- [`POST /repos/:owner/:repo/check-suites/:check_suite_id/rerequest`](/rest/reference/checks#rerequest-a-check-suite) (:gravação)
- [`PATCH /repos/:owner/:repo/check-suites/preferences`](/rest/reference/checks#update-repository-preferences-for-check-suites) (:gravação)
- [`GET /repos/:owner/:repo/commits/:sha/check-runs`](/rest/reference/checks#list-check-runs-for-a-git-reference) (:leitura)
- [`GET /repos/:owner/:repo/commits/:sha/check-suites`](/rest/reference/checks#list-check-suites-for-a-git-reference) (:leitura)

{% ifversion fpt or ghec %}
### Permissão em "codespaces"

- [`GET /repos/:owner/:repo/codespaces/machines`](/rest/reference/codespaces#list-available-machine-types-for-a-repository) {% endif %}
### Permissão em "conteúdo"

- [`GET /repos/:owner/:repo/:archive_format/:ref`](/rest/reference/repos#download-a-repository-archive) (:leitura) {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/artifacts/:artifact_id`](/rest/reference/actions#get-an-artifact) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /repos/:owner/:repo/actions/artifacts/:artifact_id`](/rest/reference/actions#delete-an-artifact) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/artifacts/:artifact_id/zip`](/rest/reference/actions#download-an-artifact) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/jobs/:job_id`](/rest/reference/actions#get-a-job-for-a-workflow-run) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/jobs/:job_id/logs`](/rest/reference/actions#download-job-logs-for-a-workflow-run) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/runs`](/rest/reference/actions#list-workflow-runs-for-a-repository) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/runs/:run_id`](/rest/reference/actions#get-a-workflow-run) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/runs/:run_id/artifacts`](/rest/reference/actions#list-workflow-run-artifacts) (:leitura) {% endif -%} {% ifversion fpt -%}
- [`POST /repos/:owner/:repo/actions/runs/:run_id/cancel`](/rest/reference/actions#cancel-a-workflow-run) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/runs/:run_id/jobs`](/rest/reference/actions#list-jobs-for-a-workflow-run) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/runs/:run_id/logs`](/rest/reference/actions#download-workflow-run-logs) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /repos/:owner/:repo/actions/runs/:run_id/logs`](/rest/reference/actions#delete-workflow-run-logs) (:gravação) {% endif -%} {% ifversion fpt -%}
- [`POST /repos/:owner/:repo/actions/runs/:run_id/rerun`](/rest/reference/actions#re-run-a-workflow) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/secrets`](/rest/reference/actions#list-repository-secrets) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/secrets/:name`](/rest/reference/actions#get-a-repository-secret) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`PUT /repos/:owner/:repo/actions/secrets/:name`](/rest/reference/actions#create-or-update-a-repository-secret) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /repos/:owner/:repo/actions/secrets/:name`](/rest/reference/actions#delete-a-repository-secret) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/secrets/public-key`](/rest/reference/actions#get-a-repository-public-key) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/workflows`](/rest/reference/actions#list-repository-workflows) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/workflows/:workflow_id`](/rest/reference/actions#get-a-workflow) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/actions/workflows/:workflow_id/runs`](/rest/reference/actions#list-workflow-runs) (:leitura) {% endif -%}
- [`GET /repos/:owner/:repo/check-runs/:check_run_id`](/rest/reference/checks#get-a-check-run) (:leitura)
- [`GET /repos/:owner/:repo/check-runs/:check_run_id/annotations`](/rest/reference/checks#list-check-run-annotations) (:leitura)
- [`GET /repos/:owner/:repo/check-suites/:check_suite_id`](/rest/reference/checks#get-a-check-suite) (:leitura)
- [`GET /repos/:owner/:repo/check-suites/:check_suite_id/check-runs`](/rest/reference/checks#list-check-runs-in-a-check-suite) (:leitura)
- [`POST /repos/:owner/:repo/check-suites/:check_suite_id/rerequest`](/rest/reference/checks#rerequest-a-check-suite) (:gravação) {% ifversion codeowners-errors %}
- [`GET /repos/:owner/:repo/codeowners/errors`](/rest/reference/repos#list-codeowners-errors) (:leitura) {% endif %}
- [`GET /repos/:owner/:repo/commits`](/rest/reference/commits#list-commits) (:leitura)
- [`GET /repos/:owner/:repo/commits/:sha`](/rest/reference/commits#get-a-commit) (:leitura)
- [`GET /repos/:owner/:repo/commits/:sha/check-runs`](/rest/reference/checks#list-check-runs-for-a-git-reference) (:leitura)
- [`GET /repos/:owner/:repo/commits/:sha/check-suites`](/rest/reference/checks#list-check-suites-for-a-git-reference) (:leitura)
- [`GET /repos/:owner/:repo/community/code_of_conduct`](/rest/reference/codes-of-conduct#get-the-code-of-conduct-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/compare/:base...:head`](/rest/reference/commits#compare-two-commits) (:leitura)
- [`GET /repos/:owner/:repo/contents/:path`](/rest/reference/repos#get-repository-content) (:leitura)
- [`POST /repos/:owner/:repo/dispatches`](/rest/reference/repos#create-a-repository-dispatch-event) (:gravação)
- [`POST /repos/:owner/:repo/forks`](/rest/reference/repos#create-a-fork) (:leitura)
- [`POST /repos/:owner/:repo/merges`](/rest/reference/branches#merge-a-branch) (:gravação)
- [`PUT /repos/:owner/:repo/pulls/:pull_number/merge`](/rest/reference/pulls#merge-a-pull-request) (:gravação)
- [`GET /repos/:owner/:repo/readme(?:/(.*))?`](/rest/reference/repos#get-a-repository-readme) (:leitura)

_Branches_
- [`GET /repos/:owner/:repo/branches`](/rest/reference/branches#list-branches) (:leitura)
- [`GET /repos/:owner/:repo/branches/:branch`](/rest/reference/branches#get-a-branch) (:leitura)
- [`GET /repos/:owner/:repo/branches/:branch/protection/restrictions/apps`](/rest/reference/repos#list-apps-with-access-to-the-protected-branch) (:gravação)
- [`POST /repos/:owner/:repo/branches/:branch/protection/restrictions/apps`](/rest/reference/branches#add-app-access-restrictions) (:gravação)
- [`PUT /repos/:owner/:repo/branches/:branch/protection/restrictions/apps`](/rest/reference/branches#set-app-access-restrictions) (:gravação)
- [`DELETE /repos/:owner/:repo/branches/:branch/protection/restrictions/apps`](/rest/reference/branches#remove-user-access-restrictions) (:gravação)
- [`POST /repos/:owner/:repo/branches/:branch/rename`](/rest/reference/branches#rename-a-branch) (:gravação)

_Comentários sobre um commit_
- [`PATCH /repos/:owner/:repo/comments/:comment_id`](/rest/reference/commits#update-a-commit-comment) (:gravação)
- [`DELETE /repos/:owner/:repo/comments/:comment_id`](/rest/reference/commits#delete-a-commit-comment) (:gravação)
- [`POST /repos/:owner/:repo/comments/:comment_id/reactions`](/rest/reference/reactions#create-reaction-for-a-commit-comment) (:gravação)
- [`POST /repos/:owner/:repo/commits/:sha/comments`](/rest/reference/commits#create-a-commit-comment) (:gravação)

_Git_
- [`POST /repos/:owner/:repo/git/blobs`](/rest/reference/git#create-a-blob) (:gravação)
- [`GET /repos/:owner/:repo/git/blobs/:sha`](/rest/reference/git#get-a-blob) (:leitura)
- [`POST /repos/:owner/:repo/git/commits`](/rest/reference/git#create-a-commit) (:gravação)
- [`GET /repos/:owner/:repo/git/commits/:commit_id`](/rest/reference/git#get-a-commit) (:leitura)
- [`POST /repos/:owner/:repo/git/refs`](/rest/reference/git#create-a-reference) (:gravação)
- [`GET /repos/:owner/:repo/git/ref/:ref`](/rest/reference/git#get-a-reference) (:leitura)
- [`GET /repos/:owner/:repo/git/matching-refs/:ref`](/rest/reference/git#list-matching-references) (:leitura)
- [`PATCH /repos/:owner/:repo/git/refs/:ref`](/rest/reference/git#update-a-reference) (:gravação)
- [`DELETE /repos/:owner/:repo/git/refs/:ref`](/rest/reference/git#delete-a-reference) (:gravação)
- [`POST /repos/:owner/:repo/git/tags`](/rest/reference/git#create-a-tag-object) (:gravação)
- [`GET /repos/:owner/:repo/git/tags/:tag_id`](/rest/reference/git#get-a-tag) (:leitura)
- [`POST /repos/:owner/:repo/git/trees`](/rest/reference/git#create-a-tree) (:gravação)
- [`GET /repos/:owner/:repo/git/trees/:sha`](/rest/reference/git#get-a-tree) (:leitura)

{% ifversion fpt or ghec %} _Importação_
- [`GET /repos/:owner/:repo/import`](/rest/reference/migrations#get-an-import-status) (:leitura)
- [`PUT /repos/:owner/:repo/import`](/rest/reference/migrations#start-an-import) (:gravação)
- [`PATCH /repos/:owner/:repo/import`](/rest/reference/migrations#update-an-import) (:gravação)
- [`DELETE /repos/:owner/:repo/import`](/rest/reference/migrations#cancel-an-import) (:gravação)
- [`GET /repos/:owner/:repo/import/authors`](/rest/reference/migrations#get-commit-authors) (:leitura)
- [`PATCH /repos/:owner/:repo/import/authors/:author_id`](/rest/reference/migrations#map-a-commit-author) (:gravação)
- [`GET /repos/:owner/:repo/import/large_files`](/rest/reference/migrations#get-large-files) (:leitura)
- [`PATCH /repos/:owner/:repo/import/lfs`](/rest/reference/migrations#update-git-lfs-preference) (:gravação) {% endif %}

_Reações_

- [`DELETE /reactions/:reaction_id`](/rest/reference/reactions#delete-a-reaction-legacy) (:gravação)
- [`DELETE /repos/:owner/:repo/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-a-commit-comment-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/reactions/:reaction_id`](/rest/reference/reactions#delete-an-issue-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-an-issue-comment-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/pulls/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-a-pull-request-comment-reaction) (:gravação)
- [`DELETE /orgs/:org/teams/:team_slug/discussions/:discussion_number/reactions/:reaction_id`](/rest/reference/reactions#delete-team-discussion-reaction) (:gravação)
- [`DELETE /orgs/:org/teams/:team_slug/discussions/:discussion_number/comments/:comment_number/reactions/:reaction_id`](/rest/reference/reactions#delete-team-discussion-comment-reaction) (:gravação)

_Versões_
- [`GET /repos/:owner/:repo/releases`](/rest/reference/repos/#list-releases) (:leitura)
- [`POST /repos/:owner/:repo/releases`](/rest/reference/repos/#create-a-release) (:gravação)
- [`GET /repos/:owner/:repo/releases/:release_id`](/rest/reference/repos/#get-a-release) (:leitura)
- [`PATCH /repos/:owner/:repo/releases/:release_id`](/rest/reference/repos/#update-a-release) (:gravação)
- [`DELETE /repos/:owner/:repo/releases/:release_id`](/rest/reference/repos/#delete-a-release) (:gravação)
- [`GET /repos/:owner/:repo/releases/:release_id/assets`](/rest/reference/repos/#list-release-assets) (:leitura)
- [`GET /repos/:owner/:repo/releases/assets/:asset_id`](/rest/reference/repos/#get-a-release-asset) (:leitura)
- [`PATCH /repos/:owner/:repo/releases/assets/:asset_id`](/rest/reference/repos/#update-a-release-asset) (:gravação)
- [`DELETE /repos/:owner/:repo/releases/assets/:asset_id`](/rest/reference/repos/#delete-a-release-asset) (:gravação)
- [`GET /repos/:owner/:repo/releases/latest`](/rest/reference/repos/#get-the-latest-release) (:leitura)
- [`GET /repos/:owner/:repo/releases/tags/:tag`](/rest/reference/repos/#get-a-release-by-tag-name) (:leitura)

### Permissão em "implantações"

- [`GET /repos/:owner/:repo/deployments`](/rest/reference/deployments#list-deployments) (:leitura)
- [`POST /repos/:owner/:repo/deployments`](/rest/reference/deployments#create-a-deployment) (:gravação)
- [`GET /repos/:owner/:repo/deployments/:deployment_id`](/rest/reference/deployments#get-a-deployment) (:leitura)
- [`DELETE /repos/:owner/:repo/deployments/:deployment_id`](/rest/reference/deployments#delete-a-deployment) (:gravação)
- [`GET /repos/:owner/:repo/deployments/:deployment_id/statuses`](/rest/reference/deployments#list-deployment-statuses) (:leitura)
- [`POST /repos/:owner/:repo/deployments/:deployment_id/statuses`](/rest/reference/deployments#create-a-deployment-status) (:gravação)
- [`GET /repos/:owner/:repo/deployments/:deployment_id/statuses/:status_id`](/rest/reference/deployments#get-a-deployment-status) (:leitura)

{% ifversion fpt or ghes or ghec %}
### Permissão em "e-mails"

{% ifversion fpt or ghec -%}
- [`PATCH /user/email/visibility`](/rest/reference/users#set-primary-email-visibility-for-the-authenticated-user) (:gravação) {% endif -%}
- [`GET /user/emails`](/rest/reference/users#list-email-addresses-for-the-authenticated-user) (:leitura)
- [`POST /user/emails`](/rest/reference/users#add-an-email-address-for-the-authenticated-user) (:gravação)
- [`DELETE /user/emails`](/rest/reference/users#delete-an-email-address-for-the-authenticated-user) (:gravação)
- [`GET /user/public_emails`](/rest/reference/users#list-public-email-addresses-for-the-authenticated-user) (:leitura) {% endif %}

### Permissão em "seguidores"

- [`GET /user/followers`](/rest/reference/users#list-followers-of-a-user) (:leitura)
- [`GET /user/following`](/rest/reference/users#list-the-people-a-user-follows) (:leitura)
- [`GET /user/following/:username`](/rest/reference/users#check-if-a-person-is-followed-by-the-authenticated-user) (:leitura)
- [`PUT /user/following/:username`](/rest/reference/users#follow-a-user) (:gravação)
- [`DELETE /user/following/:username`](/rest/reference/users#unfollow-a-user) (:gravação)

### Permissão em "chaves gpg"

- [`GET /user/gpg_keys`](/rest/reference/users#list-gpg-keys-for-the-authenticated-user) (:leitura)
- [`POST /user/gpg_keys`](/rest/reference/users#create-a-gpg-key-for-the-authenticated-user) (:gravação)
- [`GET /user/gpg_keys/:gpg_key_id`](/rest/reference/users#get-a-gpg-key-for-the-authenticated-user) (:leitura)
- [`DELETE /user/gpg_keys/:gpg_key_id`](/rest/reference/users#delete-a-gpg-key-for-the-authenticated-user) (:gravação)

{% ifversion fpt or ghec %}
### Permissão em "limites de interação"

- [`GET /user/interaction-limits`](/rest/reference/interactions#get-interaction-restrictions-for-your-public-repositories) (:leitura)
- [`PUT /user/interaction-limits`](/rest/reference/interactions#set-interaction-restrictions-for-your-public-repositories) (:gravação)
- [`DELETE /user/interaction-limits`](/rest/reference/interactions#remove-interaction-restrictions-from-your-public-repositories) (:gravação) {% endif %}

### Permissão em "problemas"

Problemas e pull requests estão estreitamente relacionados. Para obter mais informações, confira "[Listar problemas atribuídos ao usuário autenticado](/rest/reference/issues#list-issues-assigned-to-the-authenticated-user)". Se seu aplicativo GitHub tiver permissões em problemas e não em pull requests, esses pontos de extremidade irão limitar-se a problemas. Pontos de extremidade que retornam problemas e pull requests serão filtrados. Os pontos de extremidade que permitem operações em ambos problemas e pull requests estarão restritos a problemas.

- [`GET /repos/:owner/:repo/issues`](/rest/reference/issues#list-repository-issues) (:leitura)
- [`POST /repos/:owner/:repo/issues`](/rest/reference/issues#create-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number`](/rest/reference/issues#get-an-issue) (:leitura)
- [`PATCH /repos/:owner/:repo/issues/:issue_number`](/rest/reference/issues#update-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number/comments`](/rest/reference/issues#list-issue-comments) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/comments`](/rest/reference/issues#create-an-issue-comment) (:gravação)
- [`PUT /repos/:owner/:repo/issues/:issue_number/lock`](/rest/reference/issues#lock-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/lock`](/rest/reference/issues#unlock-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number/reactions`](/rest/reference/reactions#list-reactions-for-an-issue) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/reactions`](/rest/reference/reactions#create-reaction-for-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number/timeline`](/rest/reference/issues#list-timeline-events-for-an-issue) (:leitura)
- [`GET /repos/:owner/:repo/issues/comments`](/rest/reference/issues#list-issue-comments-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/issues/comments/:comment_id`](/rest/reference/issues#get-an-issue-comment) (:leitura)
- [`PATCH /repos/:owner/:repo/issues/comments/:comment_id`](/rest/reference/issues#update-an-issue-comment) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/comments/:comment_id`](/rest/reference/issues#delete-an-issue-comment) (:gravação)
- [`GET /repos/:owner/:repo/issues/comments/:comment_id/reactions`](/rest/reference/reactions#list-reactions-for-an-issue-comment) (:leitura)
- [`POST /repos/:owner/:repo/issues/comments/:comment_id/reactions`](/rest/reference/reactions#create-reaction-for-an-issue-comment) (:gravação)

_Responsáveis_
- [`GET /repos/:owner/:repo/assignees`](/rest/reference/issues#list-assignees) (:leitura)
- [`GET /repos/:owner/:repo/assignees/:username`](/rest/reference/issues#check-if-a-user-can-be-assigned) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/assignees`](/rest/reference/issues#add-assignees-to-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/assignees`](/rest/reference/issues#remove-assignees-from-an-issue) (:gravação)

_Eventos_
- [`GET /repos/:owner/:repo/issues/:issue_number/events`](/rest/reference/issues#list-issue-events) (:leitura)
- [`GET /repos/:owner/:repo/issues/events/:event_id`](/rest/reference/issues#get-an-issue-event) (:leitura)

_Rótulos_
- [`GET /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#list-labels-for-an-issue) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#add-labels-to-an-issue) (:gravação)
- [`PUT /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#set-labels-for-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#remove-all-labels-from-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/labels/:name`](/rest/reference/issues#remove-a-label-from-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/labels`](/rest/reference/issues#list-labels-for-a-repository) (:leitura)
- [`POST /repos/:owner/:repo/labels`](/rest/reference/issues#create-a-label) (:gravação)
- [`GET /repos/:owner/:repo/labels/:name`](/rest/reference/issues#get-a-label) (:leitura)
- [`PATCH /repos/:owner/:repo/labels/:name`](/rest/reference/issues#update-a-label) (:gravação)
- [`DELETE /repos/:owner/:repo/labels/:name`](/rest/reference/issues#delete-a-label) (:gravação)

_Marcos_
- [`GET /repos/:owner/:repo/milestones`](/rest/reference/issues#list-milestones) (:leitura)
- [`POST /repos/:owner/:repo/milestones`](/rest/reference/issues#create-a-milestone) (:gravação)
- [`GET /repos/:owner/:repo/milestones/:milestone_number`](/rest/reference/issues#get-a-milestone) (:leitura)
- [`PATCH /repos/:owner/:repo/milestones/:milestone_number`](/rest/reference/issues#update-a-milestone) (:gravação)
- [`DELETE /repos/:owner/:repo/milestones/:milestone_number`](/rest/reference/issues#delete-a-milestone) (:gravação)
- [`GET /repos/:owner/:repo/milestones/:milestone_number/labels`](/rest/reference/issues#list-labels-for-issues-in-a-milestone) (:leitura)

_Reações_
- [`GET /repos/:owner/:repo/issues/comments/:comment_id/reactions`](/rest/reference/reactions#list-reactions-for-an-issue-comment) (:leitura)
- [`POST /repos/:owner/:repo/issues/comments/:comment_id/reactions`](/rest/reference/reactions#create-reaction-for-an-issue-comment) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number/reactions`](/rest/reference/reactions#list-reactions-for-an-issue) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/reactions`](/rest/reference/reactions#create-reaction-for-an-issue) (:gravação)
- [`DELETE /reactions/:reaction_id`](/rest/reference/reactions#delete-a-reaction-legacy) (:gravação)
- [`DELETE /repos/:owner/:repo/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-a-commit-comment-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/reactions/:reaction_id`](/rest/reference/reactions#delete-an-issue-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-an-issue-comment-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/pulls/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-a-pull-request-comment-reaction) (:gravação)
- [`DELETE /orgs/:org/teams/:team_slug/discussions/:discussion_number/reactions/:reaction_id`](/rest/reference/reactions#delete-team-discussion-reaction) (:gravação)
- [`DELETE /orgs/:org/teams/:team_slug/discussions/:discussion_number/comments/:comment_number/reactions/:reaction_id`](/rest/reference/reactions#delete-team-discussion-comment-reaction) (:gravação)

### Permissão em "chaves"

_Chaves_
- [`GET /user/keys`](/rest/reference/users#list-public-ssh-keys-for-the-authenticated-user) (:leitura)
- [`POST /user/keys`](/rest/reference/users#create-a-public-ssh-key-for-the-authenticated-user) (:gravação)
- [`GET /user/keys/:key_id`](/rest/reference/users#get-a-public-ssh-key-for-the-authenticated-user) (:leitura)
- [`DELETE /user/keys/:key_id`](/rest/reference/users#delete-a-public-ssh-key-for-the-authenticated-user) (:gravação)

### Permissão em "integrantes"

{% ifversion fpt or ghec -%}
- [`GET /organizations/:org_id/team/:team_id/team-sync/group-mappings`](/rest/reference/teams#list-idp-groups-for-a-team) (:gravação) {% endif -%} {% ifversion fpt or ghec  -%}
- [`PATCH /organizations/:org_id/team/:team_id/team-sync/group-mappings`](/rest/reference/teams#create-or-update-idp-group-connections) (:gravação) {% endif -%}
- [`GET /orgs/:org/outside_collaborators`](/rest/reference/orgs#list-outside-collaborators-for-an-organization) (:leitura)
- [`PUT /orgs/:org/outside_collaborators/:username`](/rest/reference/orgs#convert-an-organization-member-to-outside-collaborator) (:gravação)
- [`DELETE /orgs/:org/outside_collaborators/:username`](/rest/reference/orgs#remove-outside-collaborator-from-an-organization) (:gravação) {% ifversion fpt or ghec -%}
- [`GET /orgs/:org/team-sync/groups`](/rest/teams/team-sync#list-idp-groups-for-an-organization) (:gravação) {% endif -%}
- [`GET /orgs/:org/team/:team_id`](/rest/teams/teams#get-a-team-by-name) (:leitura) {% ifversion fpt or ghec -%}
- [`GET /scim/v2/orgs/:org/Users`](/rest/reference/scim#list-scim-provisioned-identities) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`POST /scim/v2/orgs/:org/Users`](/rest/reference/scim#provision-and-invite-a-scim-user) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /scim/v2/orgs/:org/Users/:external_identity_guid`](/rest/reference/scim#get-scim-provisioning-information-for-a-user) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`PUT /scim/v2/orgs/:org/Users/:external_identity_guid`](/rest/reference/scim#set-scim-information-for-a-provisioned-user) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`PATCH /scim/v2/orgs/:org/Users/:external_identity_guid`](/rest/reference/scim#update-an-attribute-for-a-scim-user) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /scim/v2/orgs/:org/Users/:external_identity_guid`](/rest/reference/scim#delete-a-scim-user-from-an-organization) (:gravação) {% endif %}

{% ifversion fpt or ghec %} _Convites_
- [`GET /orgs/:org/invitations`](/rest/reference/orgs#list-pending-organization-invitations) (:leitura)
- [`POST /orgs/:org/invitations`](/rest/reference/orgs#create-an-organization-invitation) (:gravação)
- [`GET /orgs/:org/invitations/:invitation_id/teams`](/rest/reference/orgs#list-organization-invitation-teams) (:leitura)
- [`GET /teams/:team_id/invitations`](/rest/reference/teams#list-pending-team-invitations) (:leitura) {% endif %}

_Membros da organização_
- [`DELETE /orgs/:org/members/:username`](/rest/reference/orgs#remove-an-organization-member) (:gravação)
- [`GET /orgs/:org/memberships/:username`](/rest/reference/orgs#get-organization-membership-for-a-user) (:leitura)
- [`PUT /orgs/:org/memberships/:username`](/rest/reference/orgs#set-organization-membership-for-a-user) (:gravação)
- [`DELETE /orgs/:org/memberships/:username`](/rest/reference/orgs#remove-organization-membership-for-a-user) (:gravação)
- [`PUT /orgs/:org/public_members/:username`](/rest/reference/orgs#set-public-organization-membership-for-the-authenticated-user) (:gravação)
- [`DELETE /orgs/:org/public_members/:username`](/rest/reference/orgs#remove-public-organization-membership-for-the-authenticated-user) (:gravação)
- [`GET /user/memberships/orgs`](/rest/reference/orgs#list-organization-memberships-for-the-authenticated-user) (:leitura)
- [`GET /user/memberships/orgs/:org`](/rest/reference/orgs#get-an-organization-membership-for-the-authenticated-user) (:leitura)
- [`PATCH /user/memberships/orgs/:org`](/rest/reference/orgs#update-an-organization-membership-for-the-authenticated-user) (:gravação)

_Membros da equipe_
- [`GET /teams/:team_id/members`](/rest/reference/teams#list-team-members) (:leitura)
- [`GET /teams/:team_id/memberships/:username`](/rest/reference/teams#get-team-membership-for-a-user) (:leitura)
- [`PUT /teams/:team_id/memberships/:username`](/rest/reference/teams#add-or-update-team-membership-for-a-user) (:gravação)
- [`DELETE /teams/:team_id/memberships/:username`](/rest/reference/teams#remove-team-membership-for-a-user) (:gravação)

_Teams_
- [`GET /orgs/:org/teams`](/rest/reference/teams#list-teams) (:leitura)
- [`POST /orgs/:org/teams`](/rest/reference/teams#create-a-team) (:gravação)
- [`GET /orgs/:org/teams/:team_slug`](/rest/reference/teams#get-a-team-by-name) (:leitura)
- [`PATCH /teams/:team_id`](/rest/reference/teams#update-a-team) (:gravação)
- [`DELETE /teams/:team_id`](/rest/reference/teams#delete-a-team) (:gravação)
- [`GET /teams/:team_id/projects`](/rest/reference/teams#list-team-projects) (:leitura)
- [`GET /teams/:team_id/projects/:project_id`](/rest/reference/teams#check-team-permissions-for-a-project) (:leitura)
- [`PUT /teams/:team_id/projects/:project_id`](/rest/reference/teams#add-or-update-team-project-permissions) (:leitura)
- [`DELETE /teams/:team_id/projects/:project_id`](/rest/reference/teams#remove-a-project-from-a-team) (:leitura)
- [`GET /teams/:team_id/repos`](/rest/reference/teams#list-team-repositories) (:leitura)
- [`GET /teams/:team_id/repos/:owner/:repo`](/rest/reference/teams#check-team-permissions-for-a-repository) (:leitura)
- [`PUT /teams/:team_id/repos/:owner/:repo`](/rest/reference/teams#add-or-update-team-repository-permissions) (:leitura)
- [`DELETE /teams/:team_id/repos/:owner/:repo`](/rest/reference/teams#remove-a-repository-from-a-team) (:gravação)
- [`GET /teams/:team_id/teams`](/rest/reference/teams#list-child-teams) (:leitura)

### Permissão em "administração da organização"

- [`PATCH /orgs/:org`](/rest/reference/orgs#update-an-organization) (:gravação) {% ifversion actions-cache-management -%}
- [`GET /orgs/:org/actions/cache/usage`](/rest/reference/actions#get-github-actions-cache-usage-for-an-organization) (:leitura)
- [`GET /orgs/:org/actions/cache/usage-by-repository`](/rest/reference/actions#list-repositories-with-github-actions-cache-usage-for-an-organization) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`GET /orgs/:org/interaction-limits`](/rest/reference/interactions#get-interaction-restrictions-for-an-organization) (:leitura) {% endif -%} {% ifversion fpt or ghec -%}
- [`PUT /orgs/:org/interaction-limits`](/rest/reference/interactions#set-interaction-restrictions-for-an-organization) (:gravação) {% endif -%} {% ifversion fpt or ghec -%}
- [`DELETE /orgs/:org/interaction-limits`](/rest/reference/interactions#remove-interaction-restrictions-for-an-organization) (:gravação) {% endif %}

### Permissão em "eventos de organização"

- [`GET /users/:username/events/orgs/:org`](/rest/reference/activity#list-organization-events-for-the-authenticated-user) (:leitura)

### Permissão em "hooks da organização"

- [`GET /orgs/:org/hooks`](/rest/reference/orgs#webhooks/#list-organization-webhooks) (:leitura)
- [`POST /orgs/:org/hooks`](/rest/reference/orgs#webhooks/#create-an-organization-webhook) (:gravação)
- [`GET /orgs/:org/hooks/:hook_id`](/rest/reference/orgs#webhooks/#get-an-organization-webhook) (:leitura)
- [`PATCH /orgs/:org/hooks/:hook_id`](/rest/reference/orgs#webhooks/#update-an-organization-webhook) (:gravação)
- [`DELETE /orgs/:org/hooks/:hook_id`](/rest/reference/orgs#webhooks/#delete-an-organization-webhook) (:gravação)
- [`POST /orgs/:org/hooks/:hook_id/pings`](/rest/reference/orgs#webhooks/#ping-an-organization-webhook) (:gravação)

_Teams_
- [`DELETE /teams/:team_id/projects/:project_id`](/rest/reference/teams#remove-a-project-from-a-team) (:leitura)

{% ifversion ghes %}
### Permissão em "hooks pre-receive da organização"

- [`GET /orgs/:org/pre-receive-hooks`](/enterprise/user/rest/reference/enterprise-admin#list-pre-receive-hooks-for-an-organization) (:leitura)
- [`GET /orgs/:org/pre-receive-hooks/:pre_receive_hook_id`](/enterprise/user/rest/reference/enterprise-admin#get-a-pre-receive-hook-for-an-organization) (:leitura)
- [`PATCH /orgs/:org/pre-receive-hooks/:pre_receive_hook_id`](/enterprise/user/rest/reference/enterprise-admin#update-pre-receive-hook-enforcement-for-an-organization) (:gravação)
- [`DELETE /orgs/:org/pre-receive-hooks/:pre_receive_hook_id`](/enterprise/user/rest/reference/enterprise-admin#remove-pre-receive-hook-enforcement-for-an-organization) (:gravação) {% endif %}

### Permissão em "projetos da organização"

- [`POST /orgs/:org/projects`](/rest/reference/projects#create-an-organization-project) (:gravação)
- [`GET /projects/:project_id`](/rest/reference/projects#get-a-project) (:leitura)
- [`PATCH /projects/:project_id`](/rest/reference/projects#update-a-project) (:gravação)
- [`DELETE /projects/:project_id`](/rest/reference/projects#delete-a-project) (:gravação)
- [`POST /projects/:project_id/cards`](/rest/reference/projects#create-a-project-card) (:gravação)
- [`GET /projects/:project_id/columns`](/rest/reference/projects#list-project-columns) (:leitura)
- [`POST /projects/:project_id/columns`](/rest/reference/projects#create-a-project-column) (:gravação)
- [`GET /projects/columns/:column_id`](/rest/reference/projects#get-a-project-column) (:leitura)
- [`PATCH /projects/columns/:column_id`](/rest/reference/projects#update-a-project-column) (:gravação)
- [`DELETE /projects/columns/:column_id`](/rest/reference/projects#delete-a-project-column) (:gravação)
- [`GET /projects/columns/:column_id/cards`](/rest/reference/projects#list-project-cards) (:leitura)
- [`POST /projects/columns/:column_id/cards`](/rest/reference/projects#create-a-project-card) (:gravação)
- [`POST /projects/columns/:column_id/moves`](/rest/reference/projects#move-a-project-column) (:gravação)
- [`GET /projects/columns/cards/:card_id`](/rest/reference/projects#get-a-project-card) (:leitura)
- [`PATCH /projects/columns/cards/:card_id`](/rest/reference/projects#update-a-project-card) (:gravação)
- [`DELETE /projects/columns/cards/:card_id`](/rest/reference/projects#delete-a-project-card) (:gravação)
- [`POST /projects/columns/cards/:card_id/moves`](/rest/reference/projects#move-a-project-card) (:gravação)

{% ifversion fpt or ghec %}
### Permissão em "bloqueio de usuários da organização"

- [`GET /orgs/:org/blocks`](/rest/reference/orgs#list-users-blocked-by-an-organization) (:leitura)
- [`GET /orgs/:org/blocks/:username`](/rest/reference/orgs#check-if-a-user-is-blocked-by-an-organization) (:leitura)
- [`PUT /orgs/:org/blocks/:username`](/rest/reference/orgs#block-a-user-from-an-organization) (:gravação)
- [`DELETE /orgs/:org/blocks/:username`](/rest/reference/orgs#unblock-a-user-from-an-organization) (:gravação) {% endif %}

### Permissão em "páginas"

- [`GET /repos/:owner/:repo/pages`](/rest/reference/pages#get-a-github-pages-site) (:leitura)
- [`POST /repos/:owner/:repo/pages`](/rest/reference/pages#create-a-github-pages-site) (:gravação)
- [`PUT /repos/:owner/:repo/pages`](/rest/reference/pages#update-information-about-a-github-pages-site) (:gravação)
- [`DELETE /repos/:owner/:repo/pages`](/rest/reference/pages#delete-a-github-pages-site) (:gravação)
- [`GET /repos/:owner/:repo/pages/builds`](/rest/reference/pages#list-github-pages-builds) (:leitura)
- [`POST /repos/:owner/:repo/pages/builds`](/rest/reference/pages#request-a-github-pages-build) (:gravação)
- [`GET /repos/:owner/:repo/pages/builds/:build_id`](/rest/reference/pages#get-github-pages-build) (:leitura)
- [`GET /repos/:owner/:repo/pages/builds/latest`](/rest/reference/pages#get-latest-pages-build) (:leitura) {% ifversion fpt or ghec -%}
- [`GET /repos/:owner/:repo/pages/health`](/rest/reference/pages#get-a-dns-health-check-for-github-pages) (:gravação)
- [`POST /repos/:owner/:repo/pages/deployment`](/rest/reference/repos#create-a-github-pages-deployment) (:gravação) {% endif %}

### Permissão em "pull requests"

As solicitações de pull e os problemas estão intimamente relacionados. If your GitHub App has permissions on pull requests but not on issues, these endpoints will be limited to pull requests. Os pontos de extremidade que retornam pull requests e problemas serão filtrados. Os pontos de extremidade que permitem operações em pull requests e problemas serão restritos a pull requests.

- [`PATCH /repos/:owner/:repo/issues/:issue_number`](/rest/reference/issues#update-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number/comments`](/rest/reference/issues#list-issue-comments) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/comments`](/rest/reference/issues#create-an-issue-comment) (:gravação)
- [`PUT /repos/:owner/:repo/issues/:issue_number/lock`](/rest/reference/issues#lock-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/lock`](/rest/reference/issues#unlock-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/:issue_number/timeline`](/rest/reference/issues#list-timeline-events-for-an-issue) (:leitura)
- [`GET /repos/:owner/:repo/issues/comments`](/rest/reference/issues#list-issue-comments-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/issues/comments/:comment_id`](/rest/reference/issues#get-an-issue-comment) (:leitura)
- [`PATCH /repos/:owner/:repo/issues/comments/:comment_id`](/rest/reference/issues#update-an-issue-comment) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/comments/:comment_id`](/rest/reference/issues#delete-an-issue-comment) (:gravação)
- [`GET /repos/:owner/:repo/pulls`](/rest/reference/pulls#list-pull-requests) (:leitura)
- [`POST /repos/:owner/:repo/pulls`](/rest/reference/pulls#create-a-pull-request) (:gravação)
- [`GET /repos/:owner/:repo/pulls/:pull_number`](/rest/reference/pulls#get-a-pull-request) (:leitura)
- [`PATCH /repos/:owner/:repo/pulls/:pull_number`](/rest/reference/pulls#update-a-pull-request) (:gravação)
- [`GET /repos/:owner/:repo/pulls/:pull_number/comments`](/rest/reference/pulls#list-review-comments-on-a-pull-request) (:leitura)
- [`POST /repos/:owner/:repo/pulls/:pull_number/comments`](/rest/reference/pulls#create-a-review-comment-for-a-pull-request) (:gravação)
- [`GET /repos/:owner/:repo/pulls/:pull_number/commits`](/rest/reference/pulls#list-commits-on-a-pull-request) (:leitura)
- [`GET /repos/:owner/:repo/pulls/:pull_number/files`](/rest/reference/pulls#list-pull-requests-files) (:leitura)
- [`GET /repos/:owner/:repo/pulls/:pull_number/merge`](/rest/reference/pulls#check-if-a-pull-request-has-been-merged) (:leitura)
- [`GET /repos/:owner/:repo/pulls/comments`](/rest/reference/pulls#list-review-comments-in-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/pulls/comments/:comment_id`](/rest/reference/pulls#get-a-review-comment-for-a-pull-request) (:leitura)
- [`PATCH /repos/:owner/:repo/pulls/comments/:comment_id`](/rest/reference/pulls#update-a-review-comment-for-a-pull-request) (:gravação)
- [`DELETE /repos/:owner/:repo/pulls/comments/:comment_id`](/rest/reference/pulls#delete-a-review-comment-for-a-pull-request) (:gravação)

_Responsáveis_
- [`GET /repos/:owner/:repo/assignees`](/rest/reference/issues#list-assignees) (:leitura)
- [`GET /repos/:owner/:repo/assignees/:username`](/rest/reference/issues#check-if-a-user-can-be-assigned) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/assignees`](/rest/reference/issues#add-assignees-to-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/assignees`](/rest/reference/issues#remove-assignees-from-an-issue) (:gravação)

_Eventos_
- [`GET /repos/:owner/:repo/issues/:issue_number/events`](/rest/reference/issues#list-issue-events) (:leitura)
- [`GET /repos/:owner/:repo/issues/events/:event_id`](/rest/reference/issues#get-an-issue-event) (:leitura)
- [`POST /repos/:owner/:repo/pulls/:pull_number/reviews/:review_id/events`](/rest/reference/pulls#submit-a-review-for-a-pull-request) (:gravação)

_Rótulos_
- [`GET /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#list-labels-for-an-issue) (:leitura)
- [`POST /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#add-labels-to-an-issue) (:gravação)
- [`PUT /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#set-labels-for-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/labels`](/rest/reference/issues#remove-all-labels-from-an-issue) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/labels/:name`](/rest/reference/issues#remove-a-label-from-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/labels`](/rest/reference/issues#list-labels-for-a-repository) (:leitura)
- [`POST /repos/:owner/:repo/labels`](/rest/reference/issues#create-a-label) (:gravação)
- [`GET /repos/:owner/:repo/labels/:name`](/rest/reference/issues#get-a-label) (:leitura)
- [`PATCH /repos/:owner/:repo/labels/:name`](/rest/reference/issues#update-a-label) (:gravação)
- [`DELETE /repos/:owner/:repo/labels/:name`](/rest/reference/issues#delete-a-label) (:gravação)

_Marcos_
- [`GET /repos/:owner/:repo/milestones`](/rest/reference/issues#list-milestones) (:leitura)
- [`POST /repos/:owner/:repo/milestones`](/rest/reference/issues#create-a-milestone) (:gravação)
- [`GET /repos/:owner/:repo/milestones/:milestone_number`](/rest/reference/issues#get-a-milestone) (:leitura)
- [`PATCH /repos/:owner/:repo/milestones/:milestone_number`](/rest/reference/issues#update-a-milestone) (:gravação)
- [`DELETE /repos/:owner/:repo/milestones/:milestone_number`](/rest/reference/issues#delete-a-milestone) (:gravação)
- [`GET /repos/:owner/:repo/milestones/:milestone_number/labels`](/rest/reference/issues#list-labels-for-issues-in-a-milestone) (:leitura)

_Reações_
- [`POST /repos/:owner/:repo/issues/:issue_number/reactions`](/rest/reference/reactions#create-reaction-for-an-issue) (:gravação)
- [`GET /repos/:owner/:repo/issues/comments/:comment_id/reactions`](/rest/reference/reactions#list-reactions-for-an-issue-comment) (:leitura)
- [`POST /repos/:owner/:repo/issues/comments/:comment_id/reactions`](/rest/reference/reactions#create-reaction-for-an-issue-comment) (:gravação)
- [`GET /repos/:owner/:repo/pulls/comments/:comment_id/reactions`](/rest/reference/reactions#list-reactions-for-a-pull-request-review-comment) (:leitura)
- [`POST /repos/:owner/:repo/pulls/comments/:comment_id/reactions`](/rest/reference/reactions#create-reaction-for-a-pull-request-review-comment) (:gravação)
- [`DELETE /reactions/:reaction_id`](/rest/reference/reactions#delete-a-reaction-legacy) (:gravação)
- [`DELETE /repos/:owner/:repo/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-a-commit-comment-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/:issue_number/reactions/:reaction_id`](/rest/reference/reactions#delete-an-issue-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/issues/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-an-issue-comment-reaction) (:gravação)
- [`DELETE /repos/:owner/:repo/pulls/comments/:comment_id/reactions/:reaction_id`](/rest/reference/reactions#delete-a-pull-request-comment-reaction) (:gravação)
- [`DELETE /orgs/:org/teams/:team_slug/discussions/:discussion_number/reactions/:reaction_id`](/rest/reference/reactions#delete-team-discussion-reaction) (:gravação)
- [`DELETE /orgs/:org/teams/:team_slug/discussions/:discussion_number/comments/:comment_number/reactions/:reaction_id`](/rest/reference/reactions#delete-team-discussion-comment-reaction) (:gravação)

_Revisores solicitados_
- [`GET /repos/:owner/:repo/pulls/:pull_number/requested_reviewers`](/rest/reference/pulls#list-requested-reviewers-for-a-pull-request) (:leitura)
- [`POST /repos/:owner/:repo/pulls/:pull_number/requested_reviewers`](/rest/reference/pulls#request-reviewers-for-a-pull-request) (:gravação)
- [`DELETE /repos/:owner/:repo/pulls/:pull_number/requested_reviewers`](/rest/reference/pulls#remove-requested-reviewers-from-a-pull-request) (:gravação)

_Análises_
- [`GET /repos/:owner/:repo/pulls/:pull_number/reviews`](/rest/reference/pulls#list-reviews-for-a-pull-request) (:leitura)
- [`POST /repos/:owner/:repo/pulls/:pull_number/reviews`](/rest/reference/pulls#create-a-review-for-a-pull-request) (:gravação)
- [`GET /repos/:owner/:repo/pulls/:pull_number/reviews/:review_id`](/rest/reference/pulls#get-a-review-for-a-pull-request) (:leitura)
- [`PUT /repos/:owner/:repo/pulls/:pull_number/reviews/:review_id`](/rest/reference/pulls#update-a-review-for-a-pull-request) (:gravação)
- [`DELETE /repos/:owner/:repo/pulls/:pull_number/reviews/:review_id`](/rest/reference/pulls#delete-a-pending-review-for-a-pull-request) (:gravação)
- [`GET /repos/:owner/:repo/pulls/:pull_number/reviews/:review_id/comments`](/rest/reference/pulls#list-comments-for-a-pull-request-review) (:leitura)
- [`PUT /repos/:owner/:repo/pulls/:pull_number/reviews/:review_id/dismissals`](/rest/reference/pulls#dismiss-a-review-for-a-pull-request) (:gravação)

### Permissão em "perfil"

- [`PATCH /user`](/rest/reference/users#update-the-authenticated-user) (:gravação)

### Permissão em "hooks de repositório"

- [`GET /repos/:owner/:repo/hooks`](/rest/reference/webhooks#list-repository-webhooks) (:leitura)
- [`POST /repos/:owner/:repo/hooks`](/rest/reference/webhooks#create-a-repository-webhook) (:gravação)
- [`GET /repos/:owner/:repo/hooks/:hook_id`](/rest/reference/webhooks#get-a-repository-webhook) (:leitura)
- [`PATCH /repos/:owner/:repo/hooks/:hook_id`](/rest/reference/webhooks#update-a-repository-webhook) (:gravação)
- [`DELETE /repos/:owner/:repo/hooks/:hook_id`](/rest/reference/webhooks#delete-a-repository-webhook) (:gravação)
- [`POST /repos/:owner/:repo/hooks/:hook_id/pings`](/rest/reference/webhooks#ping-a-repository-webhook) (:leitura)
- [`POST /repos/:owner/:repo/hooks/:hook_id/tests`](/rest/reference/repos#test-the-push-repository-webhook) (:leitura)

{% ifversion ghes %}
### Permission on "repository pre receive hooks"

- [`GET /repos/:owner/:repo/pre-receive-hooks`](/enterprise/user/rest/reference/enterprise-admin#list-pre-receive-hooks-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/pre-receive-hooks/:pre_receive_hook_id`](/enterprise/user/rest/reference/enterprise-admin#get-a-pre-receive-hook-for-a-repository) (:leitura)
- [`PATCH /repos/:owner/:repo/pre-receive-hooks/:pre_receive_hook_id`](/enterprise/user/rest/reference/enterprise-admin#update-pre-receive-hook-enforcement-for-a-repository) (:gravação)
- [`DELETE /repos/:owner/:repo/pre-receive-hooks/:pre_receive_hook_id`](/enterprise/user/rest/reference/enterprise-admin#remove-pre-receive-hook-enforcement-for-a-repository) (:gravação) {% endif %}

### Permissão em "projetos de repositório"

- [`GET /projects/:project_id`](/rest/reference/projects#get-a-project) (:leitura)
- [`PATCH /projects/:project_id`](/rest/reference/projects#update-a-project) (:gravação)
- [`DELETE /projects/:project_id`](/rest/reference/projects#delete-a-project) (:gravação)
- [`POST /projects/:project_id/cards`](/rest/reference/projects#create-a-project-card) (:gravação)
- [`GET /projects/:project_id/columns`](/rest/reference/projects#list-project-columns) (:leitura)
- [`POST /projects/:project_id/columns`](/rest/reference/projects#create-a-project-column) (:gravação)
- [`GET /projects/columns/:column_id`](/rest/reference/projects#get-a-project-column) (:leitura)
- [`PATCH /projects/columns/:column_id`](/rest/reference/projects#update-a-project-column) (:gravação)
- [`DELETE /projects/columns/:column_id`](/rest/reference/projects#delete-a-project-column) (:gravação)
- [`GET /projects/columns/:column_id/cards`](/rest/reference/projects#list-project-cards) (:leitura)
- [`POST /projects/columns/:column_id/cards`](/rest/reference/projects#create-a-project-card) (:gravação)
- [`POST /projects/columns/:column_id/moves`](/rest/reference/projects#move-a-project-column) (:gravação)
- [`GET /projects/columns/cards/:card_id`](/rest/reference/projects#get-a-project-card) (:leitura)
- [`PATCH /projects/columns/cards/:card_id`](/rest/reference/projects#update-a-project-card) (:gravação)
- [`DELETE /projects/columns/cards/:card_id`](/rest/reference/projects#delete-a-project-card) (:gravação)
- [`POST /projects/columns/cards/:card_id/moves`](/rest/reference/projects#move-a-project-card) (:gravação)
- [`GET /repos/:owner/:repo/projects`](/rest/reference/projects#list-repository-projects) (:leitura)
- [`POST /repos/:owner/:repo/projects`](/rest/reference/projects#create-a-repository-project) (:gravação)

_Teams_
- [`DELETE /teams/:team_id/projects/:project_id`](/rest/reference/teams#remove-a-project-from-a-team) (:leitura)

{% ifversion fpt or ghec %}
### Permissão em "segredos"

- [`GET /repos/:owner/:repo/actions/secrets/public-key`](/rest/reference/actions#get-a-repository-public-key) (:leitura)
- [`GET /repos/:owner/:repo/actions/secrets`](/rest/reference/actions#list-repository-secrets) (:leitura)
- [`GET /repos/:owner/:repo/actions/secrets/:secret_name`](/rest/reference/actions#get-a-repository-secret) (:leitura)
- [`PUT /repos/:owner/:repo/actions/secrets/:secret_name`](/rest/reference/actions#create-or-update-a-repository-secret) (:gravação)
- [`DELETE /repos/:owner/:repo/actions/secrets/:secret_name`](/rest/reference/actions#delete-a-repository-secret) (:gravação)
- [`GET /orgs/:org/actions/secrets/public-key`](/rest/reference/actions#get-an-organization-public-key) (:leitura)
- [`GET /orgs/:org/actions/secrets`](/rest/reference/actions#list-organization-secrets) (:leitura)
- [`GET /orgs/:org/actions/secrets/:secret_name`](/rest/reference/actions#get-an-organization-secret) (:leitura)
- [`PUT /orgs/:org/actions/secrets/:secret_name`](/rest/reference/actions#create-or-update-an-organization-secret) (:gravação)
- [`GET /orgs/:org/actions/secrets/:secret_name/repositories`](/rest/reference/actions#list-selected-repositories-for-an-organization-secret) (:leitura)
- [`PUT /orgs/:org/actions/secrets/:secret_name/repositories`](/rest/reference/actions#set-selected-repositories-for-an-organization-secret) (:gravação)
- [`PUT /orgs/:org/actions/secrets/:secret_name/repositories/:repository_id`](/rest/reference/actions#add-selected-repository-to-an-organization-secret) (:gravação)
- [`DELETE /orgs/:org/actions/secrets/:secret_name/repositories/:repository_id`](/rest/reference/actions#remove-selected-repository-from-an-organization-secret) (:gravação)
- [`DELETE /orgs/:org/actions/secrets/:secret_name`](/rest/reference/actions#delete-an-organization-secret) (:gravação) {% endif %}

{% ifversion fpt or ghec or ghes > 3.3%}
### Permissão em "dependabot_secrets"
- [`GET /repos/:owner/:repo/dependabot/secrets/public-key`](/rest/reference/dependabot#get-a-repository-public-key) (:leitura)
- [`GET /repos/:owner/:repo/dependabot/secrets`](/rest/reference/dependabot#list-repository-secrets) (:leitura)
- [`GET /repos/:owner/:repo/dependabot/secrets/:secret_name`](/rest/reference/dependabot#get-a-repository-secret) (:leitura)
- [`PUT /repos/:owner/:repo/dependabot/secrets/:secret_name`](/rest/reference/dependabot#create-or-update-a-repository-secret) (:gravação)
- [`DELETE /repos/:owner/:repo/dependabot/secrets/:secret_name`](/rest/reference/dependabot#delete-a-repository-secret) (:gravação)
- [`GET /orgs/:org/dependabot/secrets/public-key`](/rest/reference/dependabot#get-an-organization-public-key) (:leitura)
- [`GET /orgs/:org/dependabot/secrets`](/rest/reference/dependabot#list-organization-secrets) (:leitura)
- [`GET /orgs/:org/dependabot/secrets/:secret_name`](/rest/reference/dependabot#get-an-organization-secret) (:leitura)
- [`PUT /orgs/:org/dependabot/secrets/:secret_name`](/rest/reference/dependabot#create-or-update-an-organization-secret) (:gravação)
- [`GET /orgs/:org/dependabot/secrets/:secret_name/repositories`](/rest/reference/dependabot#list-selected-repositories-for-an-organization-secret) (:leitura)
- [`PUT /orgs/:org/dependabot/secrets/:secret_name/repositories`](/rest/reference/dependabot#set-selected-repositories-for-an-organization-secret) (:gravação)
- [`PUT /orgs/:org/dependabot/secrets/:secret_name/repositories/:repository_id`](/rest/reference/dependabot#add-selected-repository-to-an-organization-secret) (:gravação)
- [`DELETE /orgs/:org/dependabot/secrets/:secret_name/repositories/:repository_id`](/rest/reference/dependabot#remove-selected-repository-from-an-organization-secret) (:gravação)
- [`DELETE /orgs/:org/dependabot/secrets/:secret_name`](/rest/reference/dependabot#delete-an-organization-secret) (:gravação) {% endif %}

{% ifversion ghes or ghec %}
### Permissão em "alertas de varredura de segredo"

- [`GET /repos/:owner/:repo/secret-scanning/alerts`](/rest/reference/secret-scanning#list-secret-scanning-alerts-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/secret-scanning/alerts/:alert_number`](/rest/reference/secret-scanning#get-a-secret-scanning-alert) (:leitura)
- [`PATCH /repos/:owner/:repo/secret-scanning/alerts/:alert_number`](/rest/reference/secret-scanning#update-a-secret-scanning-alert) (:gravação)
- [`GET /repos/:owner/:repo/secret-scanning/alerts/:alert_number/locations`](/rest/reference/secret-scanning#list-locations-for-a-secret-scanning-alert) (:leitura) {% endif %}

### Permissão em "eventos de segurança"

- [`GET /repos/:owner/:repo/code-scanning/alerts`](/rest/reference/code-scanning#list-code-scanning-alerts-for-a-repository) (:leitura)
- [`GET /repos/:owner/:repo/code-scanning/alerts/:alert_number`](/rest/reference/code-scanning#get-a-code-scanning-alert) (:leitura)
- [`PATCH /repos/:owner/:repo/code-scanning/alerts/:alert_number`](/rest/reference/code-scanning#update-a-code-scanning-alert) (:gravação) {% ifversion fpt or ghec or ghes or ghae -%}
- [`GET /repos/:owner/:repo/code-scanning/alerts/:alert_number/instances`](/rest/reference/code-scanning#list-instances-of-a-code-scanning-alert) (:leitura) {% endif -%}
- [`GET /repos/:owner/:repo/code-scanning/analyses`](/rest/reference/code-scanning#list-code-scanning-analyses-for-a-repository) (:leitura) {% ifversion fpt or ghec or ghes or ghae -%}
- [`GET /repos/:owner/:repo/code-scanning/analyses/:analysis_id`](/rest/reference/code-scanning#get-a-code-scanning-analysis-for-a-repository) (:leitura) {% endif -%} {% ifversion fpt or ghec or ghes -%}
- [`DELETE /repos/:owner/:repo/code-scanning/analyses/:analysis_id`](/rest/reference/code-scanning#delete-a-code-scanning-analysis-from-a-repository) (:gravação) {% endif -%}
- [`POST /repos/:owner/:repo/code-scanning/sarifs`](/rest/reference/code-scanning#upload-an-analysis-as-sarif-data) (:gravação) {% ifversion fpt or ghec or ghes or ghae -%}
- [`GET /repos/:owner/:repo/code-scanning/sarifs/:sarif_id`](/rest/reference/code-scanning#get-information-about-a-sarif-upload) (:leitura) {% endif -%} {% ifversion fpt or ghec or ghes > 3.4 or ghae-issue-5435 -%}
- [`GET /orgs/:org/code-scanning/alerts`](/rest/reference/code-scanning#list-code-scanning-alerts-by-organization) (:leitura) {% endif -%}

{% ifversion fpt or ghes or ghec %}
### Permissão em "executores auto-hospedados"
- [`GET /orgs/:org/actions/runners/downloads`](/rest/reference/actions#list-runner-applications-for-an-organization) (:leitura)
- [`POST /orgs/:org/actions/runners/registration-token`](/rest/reference/actions#create-a-registration-token-for-an-organization) (:gravação)
- [`GET /orgs/:org/actions/runners`](/rest/reference/actions#list-self-hosted-runners-for-an-organization) (:leitura)
- [`GET /orgs/:org/actions/runners/:runner_id`](/rest/reference/actions#get-a-self-hosted-runner-for-an-organization) (:leitura)
- [`POST /orgs/:org/actions/runners/remove-token`](/rest/reference/actions#create-a-remove-token-for-an-organization) (:gravação)
- [`DELETE /orgs/:org/actions/runners/:runner_id`](/rest/reference/actions#delete-a-self-hosted-runner-from-an-organization) (:gravação)
- [`GET /orgs/:org/actions/runners/:runner_id/labels`](/rest/reference/actions#list-labels-for-a-self-hosted-runner-for-an-organization) (:leitura)
- [`POST /orgs/:org/actions/runners/:runner_id/labels`](/rest/reference/actions#add-custom-labels-to-a-self-hosted-runner-for-an-organization) (:gravação)
- [`PUT /orgs/:org/actions/runners/:runner_id/labels`](/rest/reference/actions#set-custom-labels-for-a-self-hosted-runner-for-an-organization) (:gravação)
- [`DELETE /orgs/:org/actions/runners/:runner_id/labels`](/rest/reference/actions#remove-all-custom-labels-from-a-self-hosted-runner-for-an-organization) (:gravação)
- [`DELETE /orgs/:org/actions/runners/:runner_id/labels/:name`](/rest/reference/actions#remove-a-custom-label-from-a-self-hosted-runner-for-an-organization) (:gravação) {% endif %}

### Permissão em "arquivo único"

- [`GET /repos/:owner/:repo/contents/:path`](/rest/reference/repos#get-repository-content) (:leitura)
- [`PUT /repos/:owner/:repo/contents/:path`](/rest/reference/repos#create-or-update-file-contents) (:gravação)
- [`DELETE /repos/:owner/:repo/contents/:path`](/rest/reference/repos#delete-a-file) (:gravação)

### Permissão em "marcar com uma estrela"

- [`GET /user/starred/:owner/:repo`](/rest/reference/activity#check-if-a-repository-is-starred-by-the-authenticated-user) (:leitura)
- [`PUT /user/starred/:owner/:repo`](/rest/reference/activity#star-a-repository-for-the-authenticated-user) (:gravação)
- [`DELETE /user/starred/:owner/:repo`](/rest/reference/activity#unstar-a-repository-for-the-authenticated-user) (:gravação)

### Permissão em "status"

- [`GET /repos/:owner/:repo/commits/:ref/status`](/rest/reference/commits#get-the-combined-status-for-a-specific-reference) (:leitura)
- [`GET /repos/:owner/:repo/commits/:ref/statuses`](/rest/reference/commits#list-commit-statuses-for-a-reference) (:leitura)
- [`POST /repos/:owner/:repo/statuses/:sha`](/rest/reference/commits#create-a-commit-status) (:gravação)

### Permissão em "discussões em equipe"

- [`GET /teams/:team_id/discussions`](/rest/reference/teams#list-discussions) (:leitura)
- [`POST /teams/:team_id/discussions`](/rest/reference/teams#create-a-discussion) (:gravação)
- [`GET /teams/:team_id/discussions/:discussion_number`](/rest/reference/teams#get-a-discussion) (:leitura)
- [`PATCH /teams/:team_id/discussions/:discussion_number`](/rest/reference/teams#update-a-discussion) (:gravação)
- [`DELETE /teams/:team_id/discussions/:discussion_number`](/rest/reference/teams#delete-a-discussion) (:gravação)
- [`GET /teams/:team_id/discussions/:discussion_number/comments`](/rest/reference/teams#list-discussion-comments) (:leitura)
- [`POST /teams/:team_id/discussions/:discussion_number/comments`](/rest/reference/teams#create-a-discussion-comment) (:gravação)
- [`GET /teams/:team_id/discussions/:discussion_number/comments/:comment_number`](/rest/reference/teams#get-a-discussion-comment) (:leitura)
- [`PATCH /teams/:team_id/discussions/:discussion_number/comments/:comment_number`](/rest/reference/teams#update-a-discussion-comment) (:gravação)
- [`DELETE /teams/:team_id/discussions/:discussion_number/comments/:comment_number`](/rest/reference/teams#delete-a-discussion-comment) (:gravação)
- [`GET /teams/:team_id/discussions/:discussion_number/comments/:comment_number/reactions`](/rest/reference/reactions#list-reactions-for-a-team-discussion-comment) (:leitura)
- [`POST /teams/:team_id/discussions/:discussion_number/comments/:comment_number/reactions`](/rest/reference/reactions#create-reaction-for-a-team-discussion-comment) (:gravação)
- [`GET /teams/:team_id/discussions/:discussion_number/reactions`](/rest/reference/reactions#list-reactions-for-a-team-discussion) (:leitura)
- [`POST /teams/:team_id/discussions/:discussion_number/reactions`](/rest/reference/reactions#create-reaction-for-a-team-discussion) (:gravação)
