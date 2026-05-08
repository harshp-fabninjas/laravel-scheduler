# Laravel Scheduler Project Guidelines

## Code Comments

### New Functions
When creating a new function, **always add a comment** above it explaining:
- **What the function does** (purpose/responsibility)
- **Parameters** (if applicable): what each parameter represents
- **Returns** (if applicable): what the function returns

**Example:**
```php
// Schedules a task to run at a specific time
// @param string $command The command to execute
// @param string $time The time to run (e.g., "10:00", "14:30")
// @return void
public function scheduleTask($command, $time)
{
    // implementation
}
```

### Comment Style
- Use single-line comments (`//`) for simple descriptions
- Use PHPDoc blocks (`/** */`) for public methods with parameters and return types
- Only document the **WHY** if non-obvious; avoid documenting the WHAT (good naming handles that)
- Don't add comments that just repeat what the code already says clearly

## Code Organization

### Laravel Conventions
- Follow Laravel naming conventions (snake_case for database tables, columns, routes)
- Use Service providers for business logic organization
- Keep Controllers lean - delegate logic to Services/Models
- Use Models for database interactions

### Git Commits
- Write clear, descriptive commit messages
- Include the reason/motivation for changes when not obvious
- Reference related issues if applicable

## PR Reviews

The repository has an automated Claude PR review bot configured:
- Comment `@claude` on any PR to get an automated code review
- Reviews check for code quality, potential bugs, security issues, and improvements
- Uses Claude Haiku for fast, cost-efficient reviews

## File Structure
```
laravel-scheduler/
├── app/
│   ├── Console/Commands/     # Custom Artisan commands
│   ├── Models/               # Eloquent models
│   └── Services/             # Business logic
├── config/                   # Configuration files
├── routes/                   # Route definitions
├── tests/                    # Test files
└── CLAUDE.md                 # This file
```
