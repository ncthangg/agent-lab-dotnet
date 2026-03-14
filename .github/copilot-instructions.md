# Copilot Workspace Instructions

## Quick Start
1. Open this workspace in VS Code.
2. Ensure .NET 10 SDK is installed (`dotnet --info`).
3. Run `dotnet build SocOps/SocOps.csproj` in terminal.
4. Run `dotnet run --project SocOps/SocOps.csproj` and open the reported URL.

## Development Checklist
- [ ] `dotnet build SocOps/SocOps.csproj` passes
- [ ] App starts with `dotnet run --project SocOps/SocOps.csproj`
- [ ] UI behavior works for bingo flow
- [ ] Code is clean and uses consistent style (PascalCase for C# public APIs)

## Project Overview
**Soc Ops** is a Blazor WebAssembly social bingo game built with .NET 10. The app includes a quiz-style board, modal dialogs, game state service, and local storage persistence.

## Architecture
```
SocOps/
├── Components/     # Blazor UI components
├── Data/           # Static question data
├── Models/         # Game and board models
├── Pages/          # App pages (Home, Weather, etc.)
├── Services/       # Game logic and state management
├── wwwroot/        # Static assets and CSS
└── Program.cs      # app bootstrapping
```

## Key Commands
```bash
dotnet build SocOps/SocOps.csproj  # build
dotnet run --project SocOps/SocOps.csproj  # run dev server
# open http://localhost:5218 (or the URL shown in terminal)
```

## Code Patterns
- UI logic in `.razor` + component files
- Shared game state in `BingoGameService`
- Business rules in `BingoLogicService`
- Square data in `BingoSquareData` and `BingoLine`

## Troubleshooting
- If HTTPS cert prompts, run: `dotnet dev-certs https --trust`
- If app does not refresh after edits, stop and rerun dev server.

## Optional next tasks
- Add a new bingo question category in `Data/Questions.cs`
- Add end-of-game statistics in `Services/BingoGameService.cs`
- Add keyboard accessibility to bingo squares in `Components/BingoSquare.razor`
