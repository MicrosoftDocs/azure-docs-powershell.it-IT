---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196439"
---
# <span data-ttu-id="e12c7-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="e12c7-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="e12c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e12c7-103">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-103">Create or update an application.</span></span>

## <span data-ttu-id="e12c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e12c7-104">SYNTAX</span></span>

### <span data-ttu-id="e12c7-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e12c7-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e12c7-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="e12c7-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e12c7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e12c7-107">DESCRIPTION</span></span>
<span data-ttu-id="e12c7-108">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-108">Create or update an application.</span></span>

## <span data-ttu-id="e12c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e12c7-109">EXAMPLES</span></span>

### <span data-ttu-id="e12c7-110">Esempio 1: Creare un'applicazione Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="e12c7-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="e12c7-111">Questo comando crea un'applicazione Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="e12c7-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="e12c7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e12c7-112">PARAMETERS</span></span>

### <span data-ttu-id="e12c7-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="e12c7-113">-AppAlias</span></span>
<span data-ttu-id="e12c7-114">App Alias from start menu item</span><span class="sxs-lookup"><span data-stu-id="e12c7-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="e12c7-115">-ApplicationType</span></span>
<span data-ttu-id="e12c7-116">Tipo di risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-117">-CommandLine Argument</span><span class="sxs-lookup"><span data-stu-id="e12c7-117">-CommandLineArgument</span></span>
<span data-ttu-id="e12c7-118">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-118">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="e12c7-119">-CommandLineSetting</span></span>
<span data-ttu-id="e12c7-120">Specifica se l'applicazione pubblicata può essere avviata con argomenti della riga di comando forniti dal client, argomenti della riga di comando specificati al momento della pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e12c7-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12c7-121">-DefaultProfile</span></span>
<span data-ttu-id="e12c7-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e12c7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e12c7-123">-Description</span></span>
<span data-ttu-id="e12c7-124">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-124">Description of Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e12c7-125">-FilePath</span></span>
<span data-ttu-id="e12c7-126">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-126">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e12c7-127">-FriendlyName</span></span>
<span data-ttu-id="e12c7-128">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-128">Friendly name of Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e12c7-129">-GroupName</span></span>
<span data-ttu-id="e12c7-130">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="e12c7-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="e12c7-131">-IconIndex</span></span>
<span data-ttu-id="e12c7-132">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="e12c7-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="e12c7-133">-IconPath</span></span>
<span data-ttu-id="e12c7-134">Path to icon.</span><span class="sxs-lookup"><span data-stu-id="e12c7-134">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="e12c7-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="e12c7-136">Specifica l'ID applicazione del pacchetto per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="e12c7-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="e12c7-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="e12c7-138">Specifica il nome della famiglia di pacchetti per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="e12c7-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-139">-Name</span><span class="sxs-lookup"><span data-stu-id="e12c7-139">-Name</span></span>
<span data-ttu-id="e12c7-140">Nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="e12c7-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12c7-141">-ResourceGroupName</span></span>
<span data-ttu-id="e12c7-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e12c7-142">The name of the resource group.</span></span>
<span data-ttu-id="e12c7-143">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e12c7-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="e12c7-144">-ShowInPortal</span></span>
<span data-ttu-id="e12c7-145">Specifica se visualizzare il programma RemoteApp nel server Accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e12c7-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e12c7-146">-SubscriptionId</span></span>
<span data-ttu-id="e12c7-147">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e12c7-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e12c7-148">-Confirm</span></span>
<span data-ttu-id="e12c7-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e12c7-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12c7-150">-WhatIf</span></span>
<span data-ttu-id="e12c7-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e12c7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e12c7-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e12c7-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12c7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12c7-153">CommonParameters</span></span>
<span data-ttu-id="e12c7-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12c7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12c7-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e12c7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12c7-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="e12c7-156">INPUTS</span></span>

## <span data-ttu-id="e12c7-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e12c7-157">OUTPUTS</span></span>

### <span data-ttu-id="e12c7-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="e12c7-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="e12c7-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="e12c7-159">NOTES</span></span>

<span data-ttu-id="e12c7-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e12c7-160">ALIASES</span></span>

## <span data-ttu-id="e12c7-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e12c7-161">RELATED LINKS</span></span>

