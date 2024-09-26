<!-- @format -->

# Pull Request Title

<!--
Provide a concise and descriptive title for your PR.
Example: "Fix authentication bug in login module"
-->

## Why

<!--
Explain why this PR was made and what we aim to achieve with it.
- What problem does it solve?
- Why is this change necessary?
- Link any related issues or discussions.
-->

- Addresses issue #XYZ where users experienced a crash on login.
- Improves performance of data retrieval in the dashboard module.

## What

<!--
Describe the changes made and their impact on the codebase/project/feature.
- List new features, bug fixes, or other changes.
- Highlight any significant alterations.
-->

- Fixed null pointer exception in `AuthService`.
- Implemented caching for dashboard data.
- Updated dependencies to the latest versions.

## How

<!--
Detail the steps or approach taken to implement the changes.
- Explain the rationale behind the solution.
- Mention any design patterns or architectural changes.
-->

- Added null checks before accessing user data.
- Introduced Redis caching layer in `DashboardService`.
- Refactored code to adhere to the Repository pattern.

## How to Test

<!--
State the exact steps required to test this PR and its changes.
- Include setup instructions.
- Describe expected outcomes.
-->

1. **Setup Environment**
   - Pull the latest code from this branch.
   - Run `npm install` to update dependencies.
2. **Run Application**
   - Start the server with `npm start`.
   - Ensure Redis is running locally.
3. **Testing Steps**
   - Navigate to the login page and attempt to log in with valid credentials.
   - Verify that the dashboard loads data correctly and quickly.
   - Log out and try logging in with invalid credentials to test error handling.
4. **Automated Tests**
   - Run `npm test` to execute all unit and integration tests.
   - All tests should pass without errors.

## Screenshots (Optional)

<!--
Include screenshots or GIFs to help illustrate the changes.
-->

![Login Bug Fixed](https://link-to-screenshot.com/login-fix.png)

## Checklist

<!--
Mark items as completed by placing an 'x' inside the brackets: [x]
-->

- [ ] I have read the **CONTRIBUTING** guidelines.
- [ ] My code follows the project's coding style.
- [ ] I have performed a self-review of my code.
- [ ] I have commented my code where necessary.
- [ ] I have made corresponding changes to the documentation.
- [ ] My changes generate no new warnings.
- [ ] I have added tests that prove my fix is effective or that my feature works.
- [ ] New and existing unit tests pass locally with my changes.

## Types of Changes

<!--
Select the type(s) of changes your PR introduces.
-->

- [ ] 🐛 Bug fix (non-breaking change that fixes an issue)
- [ ] 🚀 New feature (non-breaking change that adds functionality)
- [ ] 💥 Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] 📝 Documentation update
- [ ] 🔄 Refactoring (no functional changes, no API changes)

## Related Issue

<!--
If this PR is related to or resolves an existing issue, link it here.
-->

- Resolves #XYZ

## Additional Notes (Optional)

<!--
Add any additional information that reviewers should be aware of.
-->

- This PR introduces a new dependency on Redis; ensure it is included in the deployment setup.
- Potential impact on the authentication module requires thorough testing.

## Deployment Instructions (Optional)

<!--
Provide any specific deployment steps required.
-->

- Run database migrations with `npm run migrate`.
- Update environment variables to include `REDIS_HOST` and `REDIS_PORT`.

## Reviewers

<!--
Tag team members or groups responsible for reviewing this PR.
-->

- @team-lead
- @backend-devs
