---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209746"
---
# <span data-ttu-id="bcbcf-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bcbcf-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="bcbcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbcf-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbcf-103">Creare o aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="bcbcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcbcf-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bcbcf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bcbcf-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbcf-106">Creare o aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="bcbcf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcbcf-107">EXAMPLES</span></span>

### <span data-ttu-id="bcbcf-108">Esempio 1: Creare un gruppo applicazioni desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="bcbcf-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="bcbcf-109">Questo comando crea un Gruppo Applicazioni Desktop virtuale Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="bcbcf-110">Esempio 2: Creare un gruppo applicazioni desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="bcbcf-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="bcbcf-111">Questo comando crea un Gruppo Applicazioni Desktop virtuale Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="bcbcf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcbcf-112">PARAMETERS</span></span>

### <span data-ttu-id="bcbcf-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="bcbcf-113">-ApplicationGroupType</span></span>
<span data-ttu-id="bcbcf-114">Tipo di risorsa ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcbcf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbcf-115">-DefaultProfile</span></span>
<span data-ttu-id="bcbcf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcbcf-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcbcf-117">-Description</span></span>
<span data-ttu-id="bcbcf-118">Descrizione di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bcbcf-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bcbcf-119">-FriendlyName</span></span>
<span data-ttu-id="bcbcf-120">Nome descrittivo di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bcbcf-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="bcbcf-121">-HostPoolArmPath</span></span>
<span data-ttu-id="bcbcf-122">Percorso arm HostPool di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bcbcf-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bcbcf-123">-Location</span></span>
<span data-ttu-id="bcbcf-124">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="bcbcf-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="bcbcf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bcbcf-125">-Name</span></span>
<span data-ttu-id="bcbcf-126">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="bcbcf-126">The name of the application group</span></span>

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

### <span data-ttu-id="bcbcf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbcf-127">-ResourceGroupName</span></span>
<span data-ttu-id="bcbcf-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-128">The name of the resource group.</span></span>
<span data-ttu-id="bcbcf-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bcbcf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcbcf-130">-SubscriptionId</span></span>
<span data-ttu-id="bcbcf-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bcbcf-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="bcbcf-132">-Tag</span></span>
<span data-ttu-id="bcbcf-133">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-133">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcbcf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcbcf-134">-Confirm</span></span>
<span data-ttu-id="bcbcf-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcbcf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcbcf-136">-WhatIf</span></span>
<span data-ttu-id="bcbcf-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcbcf-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcbcf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbcf-139">CommonParameters</span></span>
<span data-ttu-id="bcbcf-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbcf-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbcf-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="bcbcf-142">INPUTS</span></span>

## <span data-ttu-id="bcbcf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcbcf-143">OUTPUTS</span></span>

### <span data-ttu-id="bcbcf-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bcbcf-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="bcbcf-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="bcbcf-145">NOTES</span></span>

<span data-ttu-id="bcbcf-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bcbcf-146">ALIASES</span></span>

## <span data-ttu-id="bcbcf-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcbcf-147">RELATED LINKS</span></span>

