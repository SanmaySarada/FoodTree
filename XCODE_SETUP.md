# Xcode GitHub Setup Guide

Your FoodTree project is now properly configured for GitHub and will work seamlessly when cloned in Xcode.

## Repository
- **GitHub URL**: `https://github.com/SanmaySarada/FoodTree.git`
- **Main Branch**: `main`

## Pulling in Xcode

### Option 1: Clone via Xcode (Recommended)
1. Open Xcode
2. Go to **File** → **Clone Repository...**
3. Enter the URL: `https://github.com/SanmaySarada/FoodTree.git`
4. Choose a location and click **Clone**
5. Xcode will automatically open the project

### Option 2: Clone via Terminal
```bash
git clone https://github.com/SanmaySarada/FoodTree.git
cd FoodTree
open FoodTree/FoodTree.xcodeproj
```

## What's Configured

✅ **Xcode Project Files**
- `project.pbxproj` - Project configuration
- `project.xcworkspace/contents.xcworkspacedata` - Workspace files
- Shared data directories properly tracked

✅ **Git Ignore**
- User-specific files excluded (`xcuserdata/`, `*.xcuserstate`)
- Build artifacts excluded (`DerivedData/`, `build/`)
- Environment files excluded (`.env`)

✅ **Source Files**
- All Swift source files tracked
- All assets and resources tracked
- Configuration files tracked

## After Cloning

1. **Open the Project**: Double-click `FoodTree/FoodTree.xcodeproj`
2. **Select Target**: Choose `FoodTree` scheme
3. **Select Simulator**: Choose an iPhone simulator (e.g., iPhone 17)
4. **Build & Run**: Press `Cmd+R` or click the Play button

## Swift Package Dependencies

The project uses Swift Package Manager. Xcode will automatically resolve dependencies when you open the project:
- **Supabase Swift SDK** - Already configured in project

If packages don't resolve automatically:
1. Go to **File** → **Packages** → **Reset Package Caches**
2. Then **File** → **Packages** → **Resolve Package Versions**

## Troubleshooting

### "No such module 'Supabase'"
- Go to **File** → **Packages** → **Resolve Package Versions**
- Wait for packages to download

### Build Errors
- Clean build folder: **Product** → **Clean Build Folder** (`Cmd+Shift+K`)
- Restart Xcode
- Rebuild: **Product** → **Build** (`Cmd+B`)

### Workspace Issues
- Close Xcode
- Delete `DerivedData` folder (if exists)
- Reopen the project

## Notes

- The project uses **Info.plist** for Supabase configuration (keys are safe to commit)
- All user-specific Xcode settings are excluded from git
- The project structure follows Xcode best practices

