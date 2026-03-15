# Test Session Report

- Session ID: 20260314-111424-228
- Status: PASS
- Exit Code: 0
- Started At (UTC): 2026-03-14T03:14:24.2688133Z
- Finished At (UTC): 2026-03-14T03:14:24.5834582Z
- Duration (ms): 315
- Command: `powershell -NoProfile -ExecutionPolicy Bypass -Command "$ErrorActionPreference='Stop'; $required=@('.codex/SOUL.md','.codex/USER.md','.codex/MEMORY.md','.codex/TOOLS.md','.codex/HEARTBEAT.md','.codex/memory/2026-03-14-openclaw-setup.md'); foreach($path in $required){ if(-not (Test-Path $path)){ throw ('Missing ' + $path) } }; $agents=Get-Content -Raw 'AGENTS.md'; foreach($token in @('.codex/SOUL.md','.codex/USER.md','.codex/memory/','.codex/MEMORY.md')){ if($agents -notmatch [regex]::Escape($token)){ throw ('AGENTS missing ' + $token) } }; $valid=Get-Content -Raw 'release_valid.txt'; foreach($token in @('capability_summary:','knowledge_scope:','skills:','applicable_scenarios:','version_notes:')){ if($valid -notmatch [regex]::Escape($token)){ throw ('release_valid missing ' + $token) } }; $invalid=Get-Content -Raw 'release_invalid.txt'; foreach($token in @('knowledge_scope:','skills:','applicable_scenarios:')){ if($invalid -match [regex]::Escape($token)){ throw ('release_invalid unexpectedly contains ' + $token) } }; $memory=Get-Content -Raw '.codex/memory/2026-03-14-openclaw-setup.md'; if($memory -notmatch '已读取根'){ throw 'memory evidence missing read trace' }; $mainMemory=Get-Content -Raw '.codex/MEMORY.md'; if($mainMemory -notmatch 'OpenClaw'){ throw 'main memory missing setup trace' }; Write-Output 'PASS .codex files'; Write-Output 'PASS AGENTS order'; Write-Output 'PASS release semantics'; Write-Output 'PASS memory read write evidence'"`
- Workspace Root: `D:\code\AI\J-Agents\PortraitRpDemo`
- Session Path: `D:\code\AI\J-Agents\PortraitRpDemo\.test\20260314-111424-228`
- Run Log: `D:\code\AI\J-Agents\PortraitRpDemo\.test\20260314-111424-228\logs\test-run.log`
- TMP Files: 0 (0 bytes)
- Artifact Files: 0 (0 bytes)
- Log Size (bytes): 1610

