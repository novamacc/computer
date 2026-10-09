# Malcolm PR 1096 test material

Test cases for the OpenSearch proxy RBAC entries proposed in
cisagov/Malcolm pull request 1096. They are staged here for copying
into a Malcolm fork.

- `test_opensearch_rbac.lua` goes in `nginx/lua/` of Malcolm.
- `export_path_role_envs.patch` adds the test-only export of
  `path_role_envs` that the test needs.
- `test_opensearch_rbac.patch` is the test file as a patch.

Run from `nginx/lua/` with `lua5.4 test_opensearch_rbac.lua`. It needs
`lua5.4` and `lua-rex-pcre2`. All 46 cases pass against the two
OpenSearch entries from the pull request applied to Malcolm `main`.
