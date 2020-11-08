---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031549"
---
# <span data-ttu-id="3fb06-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="3fb06-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="3fb06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fb06-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb06-103">Descrive un'unità di personalizzazione delle immagini</span><span class="sxs-lookup"><span data-stu-id="3fb06-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="3fb06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fb06-104">SYNTAX</span></span>

### <span data-ttu-id="3fb06-105">ShellCustomizer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fb06-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="3fb06-106">Filecustomizr</span><span class="sxs-lookup"><span data-stu-id="3fb06-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="3fb06-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fb06-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="3fb06-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3fb06-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fb06-110">DESCRIPTION</span></span>
<span data-ttu-id="3fb06-111">Descrive un'unità di personalizzazione delle immagini</span><span class="sxs-lookup"><span data-stu-id="3fb06-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="3fb06-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fb06-112">EXAMPLES</span></span>

### <span data-ttu-id="3fb06-113">Esempio 1: creare un Windows Update Customizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="3fb06-114">Questo comando crea un Windows Update Customizer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="3fb06-115">Esempio 2: creare un file Customizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="3fb06-116">Questo comando crea un file Customizer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="3fb06-117">Esempio 3: creare un Customizer di PowerShell</span><span class="sxs-lookup"><span data-stu-id="3fb06-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="3fb06-118">Questo comando crea un Customizer di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3fb06-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="3fb06-119">Esempio 4: creare un riavvio di Customizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="3fb06-120">Questo comando crea un riavvio di Customizer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="3fb06-121">Esempio 5: creare una shell Customizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="3fb06-122">Questo comando crea una shell Customizer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="3fb06-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fb06-123">PARAMETERS</span></span>

### <span data-ttu-id="3fb06-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="3fb06-124">-CustomizerName</span></span>
<span data-ttu-id="3fb06-125">Nome descrittivo per specificare il contesto per il passaggio di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="3fb06-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="3fb06-126">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="3fb06-126">-Destination</span></span>
<span data-ttu-id="3fb06-127">Il percorso assoluto di un file (con le strutture di directory annidate già create) in cui verrà caricato il file (da sourceUri) nella VM.</span><span class="sxs-lookup"><span data-stu-id="3fb06-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="3fb06-128">-Filecustomizr</span><span class="sxs-lookup"><span data-stu-id="3fb06-128">-FileCustomizer</span></span>
<span data-ttu-id="3fb06-129">Carica i file in VM (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="3fb06-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="3fb06-130">Corrisponde al provisioner file di Packer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="3fb06-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3fb06-131">-Filter</span></span>
<span data-ttu-id="3fb06-132">Matrice di filtri per selezionare gli aggiornamenti da applicare.</span><span class="sxs-lookup"><span data-stu-id="3fb06-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="3fb06-133">Omettere o specificare la matrice vuota per usare il valore predefinito (nessun filtro).</span><span class="sxs-lookup"><span data-stu-id="3fb06-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="3fb06-134">Vedere link sopra per esempi e descrizione dettagliata di questo campo.</span><span class="sxs-lookup"><span data-stu-id="3fb06-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="3fb06-135">-In linea</span><span class="sxs-lookup"><span data-stu-id="3fb06-135">-Inline</span></span>
<span data-ttu-id="3fb06-136">Matrice di comandi di shell da eseguire.</span><span class="sxs-lookup"><span data-stu-id="3fb06-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="3fb06-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="3fb06-138">Esegue l'oggetto PowerShell specificato nella VM (Windows).</span><span class="sxs-lookup"><span data-stu-id="3fb06-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="3fb06-139">Corrisponde al provisioner di PowerShell di Packer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="3fb06-140">Può essere specificato esattamente uno di "scriptUri" o "inline".</span><span class="sxs-lookup"><span data-stu-id="3fb06-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="3fb06-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="3fb06-141">-RestartCheckCommand</span></span>
<span data-ttu-id="3fb06-142">Comando per verificare se il riavvio è riuscito [impostazione predefinita:''].</span><span class="sxs-lookup"><span data-stu-id="3fb06-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="3fb06-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="3fb06-143">-RestartCommand</span></span>
<span data-ttu-id="3fb06-144">Comando per eseguire il riavvio [impostazione predefinita:' shutdown/r/f/t 0/c Packer restart ']</span><span class="sxs-lookup"><span data-stu-id="3fb06-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="3fb06-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-145">-RestartCustomizer</span></span>
<span data-ttu-id="3fb06-146">Riavvia una VM e la attende per tornare online (Windows).</span><span class="sxs-lookup"><span data-stu-id="3fb06-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="3fb06-147">Corrisponde a Windows Packer-riavvia il provisioner.</span><span class="sxs-lookup"><span data-stu-id="3fb06-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="3fb06-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="3fb06-148">-RestartTimeout</span></span>
<span data-ttu-id="3fb06-149">Timeout di riavvio specificato come stringa di grandezza e unità, ad esempio "5m" (5 minuti) o "2h" (2 ore) [impostazione predefinita: "5m"].</span><span class="sxs-lookup"><span data-stu-id="3fb06-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="3fb06-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="3fb06-150">-RunElevated</span></span>
<span data-ttu-id="3fb06-151">Se specificato, lo script di PowerShell verrà eseguito con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="3fb06-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="3fb06-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="3fb06-152">-ScriptUri</span></span>
<span data-ttu-id="3fb06-153">URI dello script di shell da eseguire per la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="3fb06-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="3fb06-154">Può trattarsi di un collegamento GitHub, di un URI SAS per l'archiviazione di Azure e così via.</span><span class="sxs-lookup"><span data-stu-id="3fb06-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="3fb06-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="3fb06-155">-SearchCriterion</span></span>
<span data-ttu-id="3fb06-156">Criteri per la ricerca degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="3fb06-156">Criteria to search updates.</span></span>
<span data-ttu-id="3fb06-157">Omettere o specificare una stringa vuota per usare l'impostazione predefinita (Cerca in tutto).</span><span class="sxs-lookup"><span data-stu-id="3fb06-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="3fb06-158">Vedere link sopra per esempi e descrizione dettagliata di questo campo.</span><span class="sxs-lookup"><span data-stu-id="3fb06-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="3fb06-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="3fb06-159">-Sha256Checksum</span></span>
<span data-ttu-id="3fb06-160">Checksum SHA256 dello script di Shell fornito nel campo scriptUri.</span><span class="sxs-lookup"><span data-stu-id="3fb06-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="3fb06-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-161">-ShellCustomizer</span></span>
<span data-ttu-id="3fb06-162">Esegue uno script di shell durante la fase di personalizzazione (Linux).</span><span class="sxs-lookup"><span data-stu-id="3fb06-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="3fb06-163">Corrisponde al provisioner Shell Packer.</span><span class="sxs-lookup"><span data-stu-id="3fb06-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="3fb06-164">Può essere specificato esattamente uno di "scriptUri" o "inline".</span><span class="sxs-lookup"><span data-stu-id="3fb06-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="3fb06-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3fb06-165">-SourceUri</span></span>
<span data-ttu-id="3fb06-166">URI del file da caricare per la personalizzazione della VM.</span><span class="sxs-lookup"><span data-stu-id="3fb06-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="3fb06-167">Può trattarsi di un collegamento GitHub, di un URI SAS per l'archiviazione di Azure e così via.</span><span class="sxs-lookup"><span data-stu-id="3fb06-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="3fb06-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="3fb06-168">-UpdateLimit</span></span>
<span data-ttu-id="3fb06-169">Numero massimo di aggiornamenti da applicare alla volta.</span><span class="sxs-lookup"><span data-stu-id="3fb06-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="3fb06-170">Omettere o specificare 0 per usare il valore predefinito (1000).</span><span class="sxs-lookup"><span data-stu-id="3fb06-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="3fb06-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="3fb06-171">-ValidExitCode</span></span>
<span data-ttu-id="3fb06-172">Codici di uscita validi per lo script di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3fb06-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="3fb06-173">[Impostazione predefinita: 0].</span><span class="sxs-lookup"><span data-stu-id="3fb06-173">[Default: 0].</span></span>

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

### <span data-ttu-id="3fb06-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="3fb06-175">Installa gli aggiornamenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="3fb06-175">Installs Windows Updates.</span></span>
<span data-ttu-id="3fb06-176">Corrisponde a Packer Windows Update provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="3fb06-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="3fb06-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb06-177">CommonParameters</span></span>
<span data-ttu-id="3fb06-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb06-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb06-179">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fb06-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb06-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fb06-180">INPUTS</span></span>

## <span data-ttu-id="3fb06-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fb06-181">OUTPUTS</span></span>

### <span data-ttu-id="3fb06-182">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="3fb06-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="3fb06-183">Note</span><span class="sxs-lookup"><span data-stu-id="3fb06-183">NOTES</span></span>

<span data-ttu-id="3fb06-184">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3fb06-184">ALIASES</span></span>

## <span data-ttu-id="3fb06-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fb06-185">RELATED LINKS</span></span>

