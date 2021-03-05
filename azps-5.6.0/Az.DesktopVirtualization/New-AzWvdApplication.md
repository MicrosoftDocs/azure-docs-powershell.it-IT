---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: af0073a94401ce8c260027fcf905fd763d89326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980541"
---
# <span data-ttu-id="7d464-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="7d464-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="7d464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d464-102">SYNOPSIS</span></span>
<span data-ttu-id="7d464-103">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-103">Create or update an application.</span></span>

## <span data-ttu-id="7d464-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d464-104">SYNTAX</span></span>

### <span data-ttu-id="7d464-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d464-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7d464-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="7d464-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7d464-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d464-107">DESCRIPTION</span></span>
<span data-ttu-id="7d464-108">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-108">Create or update an application.</span></span>

## <span data-ttu-id="7d464-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d464-109">EXAMPLES</span></span>

### <span data-ttu-id="7d464-110">Esempio 1: Creare un'applicazione Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="7d464-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="7d464-111">Questo comando crea un'applicazione Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="7d464-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="7d464-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d464-112">PARAMETERS</span></span>

### <span data-ttu-id="7d464-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="7d464-113">-AppAlias</span></span>
<span data-ttu-id="7d464-114">App Alias from start menu item</span><span class="sxs-lookup"><span data-stu-id="7d464-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="7d464-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="7d464-115">-ApplicationType</span></span>
<span data-ttu-id="7d464-116">Tipo di risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="7d464-117">-CommandLine Argument</span><span class="sxs-lookup"><span data-stu-id="7d464-117">-CommandLineArgument</span></span>
<span data-ttu-id="7d464-118">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="7d464-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="7d464-119">-CommandLineSetting</span></span>
<span data-ttu-id="7d464-120">Specifica se l'applicazione pubblicata può essere avviata con argomenti della riga di comando forniti dal client, argomenti della riga di comando specificati al momento della pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7d464-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="7d464-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d464-121">-DefaultProfile</span></span>
<span data-ttu-id="7d464-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d464-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d464-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d464-123">-Description</span></span>
<span data-ttu-id="7d464-124">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-124">Description of Application.</span></span>

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

### <span data-ttu-id="7d464-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7d464-125">-FilePath</span></span>
<span data-ttu-id="7d464-126">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="7d464-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d464-127">-FriendlyName</span></span>
<span data-ttu-id="7d464-128">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="7d464-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7d464-129">-GroupName</span></span>
<span data-ttu-id="7d464-130">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="7d464-130">The name of the application group</span></span>

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

### <span data-ttu-id="7d464-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="7d464-131">-IconIndex</span></span>
<span data-ttu-id="7d464-132">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="7d464-132">Index of the icon.</span></span>

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

### <span data-ttu-id="7d464-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="7d464-133">-IconPath</span></span>
<span data-ttu-id="7d464-134">Path to icon.</span><span class="sxs-lookup"><span data-stu-id="7d464-134">Path to icon.</span></span>

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

### <span data-ttu-id="7d464-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="7d464-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="7d464-136">Specifica l'ID applicazione del pacchetto per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="7d464-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="7d464-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="7d464-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="7d464-138">Specifica il nome della famiglia di pacchetti per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="7d464-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="7d464-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7d464-139">-Name</span></span>
<span data-ttu-id="7d464-140">Nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="7d464-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="7d464-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d464-141">-ResourceGroupName</span></span>
<span data-ttu-id="7d464-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d464-142">The name of the resource group.</span></span>
<span data-ttu-id="7d464-143">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7d464-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7d464-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="7d464-144">-ShowInPortal</span></span>
<span data-ttu-id="7d464-145">Specifica se visualizzare il programma RemoteApp nel server Accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="7d464-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="7d464-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d464-146">-SubscriptionId</span></span>
<span data-ttu-id="7d464-147">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7d464-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7d464-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d464-148">-Confirm</span></span>
<span data-ttu-id="7d464-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d464-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d464-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d464-150">-WhatIf</span></span>
<span data-ttu-id="7d464-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d464-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d464-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d464-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d464-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d464-153">CommonParameters</span></span>
<span data-ttu-id="7d464-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d464-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d464-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d464-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d464-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d464-156">INPUTS</span></span>

## <span data-ttu-id="7d464-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d464-157">OUTPUTS</span></span>

### <span data-ttu-id="7d464-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="7d464-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="7d464-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d464-159">NOTES</span></span>

<span data-ttu-id="7d464-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7d464-160">ALIASES</span></span>

## <span data-ttu-id="7d464-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d464-161">RELATED LINKS</span></span>

