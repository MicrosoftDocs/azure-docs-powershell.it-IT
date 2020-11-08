---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190220"
---
# <span data-ttu-id="4188a-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4188a-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4188a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4188a-102">SYNOPSIS</span></span>
<span data-ttu-id="4188a-103">Creare o aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4188a-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="4188a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4188a-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4188a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4188a-105">DESCRIPTION</span></span>
<span data-ttu-id="4188a-106">Creare o aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4188a-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="4188a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4188a-107">EXAMPLES</span></span>

### <span data-ttu-id="4188a-108">Esempio 1: creare un desktop virtuale di Windows ApplicationGroup per nome</span><span class="sxs-lookup"><span data-stu-id="4188a-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="4188a-109">Questo comando crea un ApplicationGroup desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4188a-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="4188a-110">Esempio 2: creare un desktop virtuale di Windows ApplicationGroup per nome</span><span class="sxs-lookup"><span data-stu-id="4188a-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="4188a-111">Questo comando crea un ApplicationGroup desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4188a-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="4188a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4188a-112">PARAMETERS</span></span>

### <span data-ttu-id="4188a-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="4188a-113">-ApplicationGroupType</span></span>
<span data-ttu-id="4188a-114">Tipo di risorsa di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4188a-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4188a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4188a-115">-DefaultProfile</span></span>
<span data-ttu-id="4188a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4188a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4188a-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4188a-117">-Description</span></span>
<span data-ttu-id="4188a-118">Descrizione di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4188a-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4188a-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4188a-119">-FriendlyName</span></span>
<span data-ttu-id="4188a-120">Nome descrittivo di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4188a-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4188a-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="4188a-121">-HostPoolArmPath</span></span>
<span data-ttu-id="4188a-122">Percorso del braccio HostPool di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="4188a-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4188a-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4188a-123">-Location</span></span>
<span data-ttu-id="4188a-124">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="4188a-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="4188a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4188a-125">-Name</span></span>
<span data-ttu-id="4188a-126">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="4188a-126">The name of the application group</span></span>

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

### <span data-ttu-id="4188a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4188a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4188a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4188a-128">The name of the resource group.</span></span>
<span data-ttu-id="4188a-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4188a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4188a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4188a-130">-SubscriptionId</span></span>
<span data-ttu-id="4188a-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4188a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4188a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="4188a-132">-Tag</span></span>
<span data-ttu-id="4188a-133">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4188a-133">Resource tags.</span></span>

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

### <span data-ttu-id="4188a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4188a-134">-Confirm</span></span>
<span data-ttu-id="4188a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4188a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4188a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4188a-136">-WhatIf</span></span>
<span data-ttu-id="4188a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4188a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4188a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4188a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4188a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4188a-139">CommonParameters</span></span>
<span data-ttu-id="4188a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4188a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4188a-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4188a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4188a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4188a-142">INPUTS</span></span>

## <span data-ttu-id="4188a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4188a-143">OUTPUTS</span></span>

### <span data-ttu-id="4188a-144">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4188a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="4188a-145">Note</span><span class="sxs-lookup"><span data-stu-id="4188a-145">NOTES</span></span>

<span data-ttu-id="4188a-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4188a-146">ALIASES</span></span>

## <span data-ttu-id="4188a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4188a-147">RELATED LINKS</span></span>

