---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192512"
---
# <span data-ttu-id="86afe-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="86afe-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="86afe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86afe-102">SYNOPSIS</span></span>
<span data-ttu-id="86afe-103">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-103">Create or update an application.</span></span>

## <span data-ttu-id="86afe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86afe-104">SYNTAX</span></span>

### <span data-ttu-id="86afe-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86afe-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="86afe-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="86afe-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="86afe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86afe-107">DESCRIPTION</span></span>
<span data-ttu-id="86afe-108">Creare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-108">Create or update an application.</span></span>

## <span data-ttu-id="86afe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86afe-109">EXAMPLES</span></span>

### <span data-ttu-id="86afe-110">Esempio 1: creare un'applicazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="86afe-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="86afe-111">Questo comando crea un'applicazione desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="86afe-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="86afe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86afe-112">PARAMETERS</span></span>

### <span data-ttu-id="86afe-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="86afe-113">-AppAlias</span></span>
<span data-ttu-id="86afe-114">Alias app dalla voce di menu Start</span><span class="sxs-lookup"><span data-stu-id="86afe-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="86afe-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="86afe-115">-CommandLineArgument</span></span>
<span data-ttu-id="86afe-116">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="86afe-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="86afe-117">-CommandLineSetting</span></span>
<span data-ttu-id="86afe-118">Specifica se l'applicazione pubblicata può essere avviata con gli argomenti della riga di comando forniti dal client, gli argomenti della riga di comando specificati in fase di pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="86afe-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="86afe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86afe-119">-DefaultProfile</span></span>
<span data-ttu-id="86afe-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86afe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86afe-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="86afe-121">-Description</span></span>
<span data-ttu-id="86afe-122">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-122">Description of Application.</span></span>

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

### <span data-ttu-id="86afe-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="86afe-123">-FilePath</span></span>
<span data-ttu-id="86afe-124">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="86afe-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="86afe-125">-FriendlyName</span></span>
<span data-ttu-id="86afe-126">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="86afe-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="86afe-127">-GroupName</span></span>
<span data-ttu-id="86afe-128">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="86afe-128">The name of the application group</span></span>

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

### <span data-ttu-id="86afe-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="86afe-129">-IconIndex</span></span>
<span data-ttu-id="86afe-130">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="86afe-130">Index of the icon.</span></span>

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

### <span data-ttu-id="86afe-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="86afe-131">-IconPath</span></span>
<span data-ttu-id="86afe-132">Percorso dell'icona.</span><span class="sxs-lookup"><span data-stu-id="86afe-132">Path to icon.</span></span>

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

### <span data-ttu-id="86afe-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="86afe-133">-Name</span></span>
<span data-ttu-id="86afe-134">Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="86afe-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="86afe-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86afe-135">-ResourceGroupName</span></span>
<span data-ttu-id="86afe-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86afe-136">The name of the resource group.</span></span>
<span data-ttu-id="86afe-137">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="86afe-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="86afe-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="86afe-138">-ShowInPortal</span></span>
<span data-ttu-id="86afe-139">Specifica se visualizzare il programma RemoteApp nel server di accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="86afe-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="86afe-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86afe-140">-SubscriptionId</span></span>
<span data-ttu-id="86afe-141">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86afe-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="86afe-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86afe-142">-Confirm</span></span>
<span data-ttu-id="86afe-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86afe-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86afe-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86afe-144">-WhatIf</span></span>
<span data-ttu-id="86afe-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86afe-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86afe-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86afe-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86afe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86afe-147">CommonParameters</span></span>
<span data-ttu-id="86afe-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86afe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86afe-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86afe-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86afe-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86afe-150">INPUTS</span></span>

## <span data-ttu-id="86afe-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86afe-151">OUTPUTS</span></span>

### <span data-ttu-id="86afe-152">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="86afe-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="86afe-153">Note</span><span class="sxs-lookup"><span data-stu-id="86afe-153">NOTES</span></span>

<span data-ttu-id="86afe-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="86afe-154">ALIASES</span></span>

## <span data-ttu-id="86afe-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86afe-155">RELATED LINKS</span></span>

