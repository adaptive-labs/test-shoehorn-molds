# Shoehorn Molds Repository

This repository contains workflow templates (molds) for the Shoehorn platform.

## 📦 Available Molds

### Create GitHub Repository
**File:** `create-github-repo.json`
**Purpose:** Create a new GitHub repository with customizable settings

**Inputs:**
- `name` (required) - Repository name (lowercase, alphanumeric with dashes)
- `description` - Repository description
- `defaultBranch` - Default branch name (main, master, or develop)
- `autoInit` - Initialize repository with README (default: true)
- `private` - Create as private repository (default: true)
- `hasIssues` - Enable issues (default: true)
- `hasWiki` - Enable wiki (default: false)
- `hasProjects` - Enable projects (default: false)

**Outputs:**
- `repositoryUrl` - GitHub API URL
- `htmlUrl` - GitHub web URL
- `cloneUrl` - HTTPS clone URL
- `sshUrl` - SSH clone URL

## 📝 Mold Discovery

Shoehorn automatically discovers molds from configured repositories. Molds must:

1. Be valid JSON files
2. Follow the Shoehorn v2 workflow schema
3. Include proper metadata (name, description, category, tags)
4. Define inputs with JSON schema validation
5. Specify workflow steps with adapters

## 🚀 Usage

1. Navigate to Forge in Shoehorn
2. Browse available molds
3. Select "Create GitHub Repository"
4. Fill in the required inputs
5. Execute the workflow

## 🔧 Development

To add new molds:

1. Create a new JSON file following the v2 workflow schema
2. Define inputs, outputs, and steps
3. Test locally before committing
4. Push to this repository
5. Shoehorn will auto-discover on next sync

## 📚 Schema Reference

See the [Shoehorn Workflow v2 Schema](https://shoehorn.dev/schemas/workflow-v2.json) for full documentation.

## 🤝 Contributing

Feel free to contribute new molds! Ensure they:
- Follow the schema
- Include comprehensive descriptions
- Have sensible defaults
- Handle errors gracefully
- Include rollback steps where appropriate
