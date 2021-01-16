---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475361"
---
# <span data-ttu-id="350e3-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="350e3-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="350e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="350e3-102">SYNOPSIS</span></span>
<span data-ttu-id="350e3-103">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-103">Create or update an application.</span></span>

## <span data-ttu-id="350e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="350e3-104">SYNTAX</span></span>

### <span data-ttu-id="350e3-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="350e3-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="350e3-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="350e3-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="350e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="350e3-107">DESCRIPTION</span></span>
<span data-ttu-id="350e3-108">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-108">Create or update an application.</span></span>

## <span data-ttu-id="350e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="350e3-109">EXAMPLES</span></span>

### <span data-ttu-id="350e3-110">Esempio 1: creare un'applicazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="350e3-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="350e3-111">Questo comando crea un'applicazione desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="350e3-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="350e3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="350e3-112">PARAMETERS</span></span>

### <span data-ttu-id="350e3-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="350e3-113">-AppAlias</span></span>
<span data-ttu-id="350e3-114">Alias app dalla voce di menu Start</span><span class="sxs-lookup"><span data-stu-id="350e3-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="350e3-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="350e3-115">-ApplicationType</span></span>
<span data-ttu-id="350e3-116">Tipo di risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="350e3-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="350e3-117">-CommandLineArgument</span></span>
<span data-ttu-id="350e3-118">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="350e3-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="350e3-119">-CommandLineSetting</span></span>
<span data-ttu-id="350e3-120">Specifica se l'applicazione pubblicata può essere avviata con gli argomenti della riga di comando forniti dal client, gli argomenti della riga di comando specificati in fase di pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="350e3-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="350e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350e3-121">-DefaultProfile</span></span>
<span data-ttu-id="350e3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="350e3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="350e3-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="350e3-123">-Description</span></span>
<span data-ttu-id="350e3-124">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-124">Description of Application.</span></span>

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

### <span data-ttu-id="350e3-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="350e3-125">-FilePath</span></span>
<span data-ttu-id="350e3-126">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="350e3-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="350e3-127">-FriendlyName</span></span>
<span data-ttu-id="350e3-128">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="350e3-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="350e3-129">-GroupName</span></span>
<span data-ttu-id="350e3-130">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="350e3-130">The name of the application group</span></span>

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

### <span data-ttu-id="350e3-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="350e3-131">-IconIndex</span></span>
<span data-ttu-id="350e3-132">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="350e3-132">Index of the icon.</span></span>

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

### <span data-ttu-id="350e3-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="350e3-133">-IconPath</span></span>
<span data-ttu-id="350e3-134">Percorso dell'icona.</span><span class="sxs-lookup"><span data-stu-id="350e3-134">Path to icon.</span></span>

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

### <span data-ttu-id="350e3-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="350e3-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="350e3-136">Specifica l'ID applicazione pacchetto per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="350e3-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="350e3-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="350e3-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="350e3-138">Specifica il nome della famiglia di pacchetti per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="350e3-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="350e3-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="350e3-139">-Name</span></span>
<span data-ttu-id="350e3-140">Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="350e3-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="350e3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350e3-141">-ResourceGroupName</span></span>
<span data-ttu-id="350e3-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="350e3-142">The name of the resource group.</span></span>
<span data-ttu-id="350e3-143">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="350e3-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="350e3-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="350e3-144">-ShowInPortal</span></span>
<span data-ttu-id="350e3-145">Specifica se visualizzare il programma RemoteApp nel server di accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="350e3-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="350e3-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="350e3-146">-SubscriptionId</span></span>
<span data-ttu-id="350e3-147">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="350e3-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="350e3-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="350e3-148">-Confirm</span></span>
<span data-ttu-id="350e3-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350e3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="350e3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="350e3-150">-WhatIf</span></span>
<span data-ttu-id="350e3-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="350e3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="350e3-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="350e3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="350e3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350e3-153">CommonParameters</span></span>
<span data-ttu-id="350e3-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350e3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350e3-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="350e3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350e3-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="350e3-156">INPUTS</span></span>

## <span data-ttu-id="350e3-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="350e3-157">OUTPUTS</span></span>

### <span data-ttu-id="350e3-158">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="350e3-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="350e3-159">Note</span><span class="sxs-lookup"><span data-stu-id="350e3-159">NOTES</span></span>

<span data-ttu-id="350e3-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="350e3-160">ALIASES</span></span>

## <span data-ttu-id="350e3-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="350e3-161">RELATED LINKS</span></span>

