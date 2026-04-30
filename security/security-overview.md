## Module Security

Security is not optional. Every module that accepts user input, displays data, or interacts with the database must implement proper security measures. A single vulnerability in one module can compromise an entire CMSMS installation.

This chapter covers the security mechanisms CMSMS provides and how to use them correctly in your modules.

### In This Chapter

- [Checking Permissions](/docs/security/checking-permissions) — Control who can access your module's admin actions using the CMSMS permission system.
- [Data Validation](/docs/security/data-validation) — Verify that data meets your expectations before processing it.
- [Nonces (CSRF Protection)](/docs/security/nonces) — Protect forms and actions against cross-site request forgery attacks.
- [Securing (Escaping) Output](/docs/security/securing-output) — Prevent cross-site scripting (XSS) by escaping data before displaying it.
- [Securing (Sanitizing) Input](/docs/security/securing-input) — Clean and sanitize all input before using it in your module.

### The Golden Rules

1. **Never trust user input.** All data from forms, URLs, cookies, and HTTP headers must be validated and sanitized.
2. **Escape all output.** Any data displayed in HTML, JavaScript, or SQL must be properly escaped for its context.
3. **Check permissions on every admin action.** Do not rely on navigation visibility alone.
4. **Use parameterized queries.** Never concatenate user input into SQL strings.
5. **Protect forms with CSRF tokens.** Use the built-in Smarty form plugins that handle this automatically.
