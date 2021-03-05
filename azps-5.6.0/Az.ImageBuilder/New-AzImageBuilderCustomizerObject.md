---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 97e59efcc20f8ce025b2e90285ef051edc8272dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013054"
---
# <span data-ttu-id="a5f3d-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="a5f3d-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="a5f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f3d-103">Descrive un'unità di personalizzazione dell'immagine</span><span class="sxs-lookup"><span data-stu-id="a5f3d-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="a5f3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5f3d-104">SYNTAX</span></span>

### <span data-ttu-id="a5f3d-105">ShellCustomizer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5f3d-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="a5f3d-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="a5f3d-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5f3d-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="a5f3d-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a5f3d-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5f3d-110">DESCRIPTION</span></span>
<span data-ttu-id="a5f3d-111">Descrive un'unità di personalizzazione dell'immagine</span><span class="sxs-lookup"><span data-stu-id="a5f3d-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="a5f3d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5f3d-112">EXAMPLES</span></span>

### <span data-ttu-id="a5f3d-113">Esempio 1: Creare un programma di personalizzazione di Windows Update</span><span class="sxs-lookup"><span data-stu-id="a5f3d-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="a5f3d-114">Questo comando crea un programma di personalizzazione di Windows Update.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="a5f3d-115">Esempio 2: Creare un file personalizzatore</span><span class="sxs-lookup"><span data-stu-id="a5f3d-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="a5f3d-116">Questo comando crea un'utilità per la personalizzazione dei file.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="a5f3d-117">Esempio 3: Creare un customizer di PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5f3d-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="a5f3d-118">Questo comando crea un customizer di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="a5f3d-119">Esempio 4: Creare un riavvio della personalizzazione</span><span class="sxs-lookup"><span data-stu-id="a5f3d-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="a5f3d-120">Questo comando crea una personalizzazione di riavvio.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="a5f3d-121">Esempio 5: Creare un personalizzazione della shell</span><span class="sxs-lookup"><span data-stu-id="a5f3d-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="a5f3d-122">Questo comando crea un personalizzazione della shell.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="a5f3d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5f3d-123">PARAMETERS</span></span>

### <span data-ttu-id="a5f3d-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="a5f3d-124">-CustomizerName</span></span>
<span data-ttu-id="a5f3d-125">Nome descrittivo per fornire contesto sulla scopo di questo passaggio di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="a5f3d-126">-Destination</span></span>
<span data-ttu-id="a5f3d-127">Il percorso assoluto di un file (con strutture di directory annidate già create) in cui il file (da sourceUri) verrà caricato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-128">-FileCustomizer</span></span>
<span data-ttu-id="a5f3d-129">Carica i file nelle macchine virtuali (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="a5f3d-130">Corrisponde al provisioning file packer.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="a5f3d-131">-Filter</span></span>
<span data-ttu-id="a5f3d-132">Matrice di filtri per selezionare gli aggiornamenti da applicare.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="a5f3d-133">Omettere o specificare una matrice vuota da usare per impostazione predefinita (nessun filtro).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="a5f3d-134">Fare riferimento al collegamento precedente per esempi e una descrizione dettagliata di questo campo.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-135">-In linea</span><span class="sxs-lookup"><span data-stu-id="a5f3d-135">-Inline</span></span>
<span data-ttu-id="a5f3d-136">Matrice di comandi di shell da eseguire.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="a5f3d-138">Esegue la sessione di PowerShell specificata nella macchina virtuale (Windows).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="a5f3d-139">Corrisponde al provisioning di Packer PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="a5f3d-140">È possibile specificare esattamente uno di "scriptUri" o "inline".</span><span class="sxs-lookup"><span data-stu-id="a5f3d-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="a5f3d-141">-RestartCheckCommand</span></span>
<span data-ttu-id="a5f3d-142">Comando per verificare se il riavvio ha esito positivo [impostazione predefinita: ''].</span><span class="sxs-lookup"><span data-stu-id="a5f3d-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="a5f3d-143">-RestartCommand</span></span>
<span data-ttu-id="a5f3d-144">Comando per eseguire il riavvio [Impostazione predefinita: 'arrestato /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="a5f3d-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-145">-RestartCustomizer</span></span>
<span data-ttu-id="a5f3d-146">Riavvia una macchina virtuale e attende che torni online (Windows).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="a5f3d-147">Corrisponde al provisioning packer di windows-restart.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="a5f3d-148">-RestartTimeout</span></span>
<span data-ttu-id="a5f3d-149">Timeout di riavvio specificato come stringa di grandezza e unità, ad esempio "5m" (5 minuti) o "2h" (2 ore) [Predefinito: '5m'].</span><span class="sxs-lookup"><span data-stu-id="a5f3d-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="a5f3d-150">-RunElevated</span></span>
<span data-ttu-id="a5f3d-151">Se specificato, lo script di PowerShell verrà eseguito con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="a5f3d-152">-ScriptUri</span></span>
<span data-ttu-id="a5f3d-153">URI dello script della shell da eseguire per la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="a5f3d-154">Può essere un collegamento a github, un URI di firma di accesso condiviso per Archiviazione di Azure e così via.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="a5f3d-155">-SearchCriterion</span></span>
<span data-ttu-id="a5f3d-156">Criteri per cercare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-156">Criteria to search updates.</span></span>
<span data-ttu-id="a5f3d-157">Omettere o specificare una stringa vuota per usare la stringa predefinita (cerca in tutti).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="a5f3d-158">Fare riferimento al collegamento precedente per esempi e una descrizione dettagliata di questo campo.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="a5f3d-159">-Sha256Checksum</span></span>
<span data-ttu-id="a5f3d-160">Checksum SHA256 dello script della shell fornito nel campo scriptUri.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-161">-ShellCustomizer</span></span>
<span data-ttu-id="a5f3d-162">Esegue uno script della shell durante la fase di personalizzazione (Linux).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="a5f3d-163">Corrisponde al provisioning della shell packer.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="a5f3d-164">È possibile specificare esattamente uno di "scriptUri" o "inline".</span><span class="sxs-lookup"><span data-stu-id="a5f3d-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a5f3d-165">-SourceUri</span></span>
<span data-ttu-id="a5f3d-166">URI del file da caricare per personalizzare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="a5f3d-167">Può essere un collegamento a github, un URI di firma di accesso condiviso per Archiviazione di Azure e così via.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="a5f3d-168">-UpdateLimit</span></span>
<span data-ttu-id="a5f3d-169">Numero massimo di aggiornamenti da applicare alla volta.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="a5f3d-170">Omettere o specificare 0 per usare il valore predefinito (1000).</span><span class="sxs-lookup"><span data-stu-id="a5f3d-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="a5f3d-171">-ValidExitCode</span></span>
<span data-ttu-id="a5f3d-172">Codici di uscita validi per lo script di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="a5f3d-173">[Impostazione predefinita: 0].</span><span class="sxs-lookup"><span data-stu-id="a5f3d-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="a5f3d-175">Installa gli aggiornamenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-175">Installs Windows Updates.</span></span>
<span data-ttu-id="a5f3d-176">Corrisponde al provisioning di Windows Update Packer ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="a5f3d-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f3d-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f3d-177">CommonParameters</span></span>
<span data-ttu-id="a5f3d-178">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f3d-179">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5f3d-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f3d-180">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5f3d-180">INPUTS</span></span>

## <span data-ttu-id="a5f3d-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5f3d-181">OUTPUTS</span></span>

### <span data-ttu-id="a5f3d-182">Microsoft.Azure.PowerShell.Cmdlets.ImageMag.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="a5f3d-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="a5f3d-183">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5f3d-183">NOTES</span></span>

<span data-ttu-id="a5f3d-184">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a5f3d-184">ALIASES</span></span>

## <span data-ttu-id="a5f3d-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5f3d-185">RELATED LINKS</span></span>

