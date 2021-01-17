---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384565"
---
# <span data-ttu-id="7ea45-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7ea45-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7ea45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ea45-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea45-103">Imposta o aggiorna un prefisso registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="7ea45-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="7ea45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ea45-104">SYNTAX</span></span>

### <span data-ttu-id="7ea45-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ea45-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea45-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7ea45-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea45-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea45-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea45-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ea45-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea45-109">Consente l'aggiornamento di un prefisso registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="7ea45-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="7ea45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ea45-110">EXAMPLES</span></span>

### <span data-ttu-id="7ea45-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ea45-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="7ea45-112">Aggiorna il prefisso per ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7ea45-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="7ea45-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ea45-113">PARAMETERS</span></span>

### <span data-ttu-id="7ea45-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ea45-114">-AsJob</span></span>
<span data-ttu-id="7ea45-115">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="7ea45-115">Run in the background.</span></span>

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

### <span data-ttu-id="7ea45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea45-116">-DefaultProfile</span></span>
<span data-ttu-id="7ea45-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ea45-118">-InputObject</span></span>
<span data-ttu-id="7ea45-119">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="7ea45-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ea45-120">-Name</span></span>
<span data-ttu-id="7ea45-121">Il nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="7ea45-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="7ea45-122">-PeeringName</span></span>
<span data-ttu-id="7ea45-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7ea45-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="7ea45-124">-Prefix</span></span>
<span data-ttu-id="7ea45-125">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="7ea45-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="7ea45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea45-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ea45-127">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="7ea45-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea45-128">-ResourceId</span></span>
<span data-ttu-id="7ea45-129">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7ea45-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ea45-130">-Confirm</span></span>
<span data-ttu-id="7ea45-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea45-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea45-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea45-132">-WhatIf</span></span>
<span data-ttu-id="7ea45-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ea45-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea45-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ea45-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea45-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea45-135">CommonParameters</span></span>
<span data-ttu-id="7ea45-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea45-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea45-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ea45-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea45-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ea45-138">INPUTS</span></span>

### <span data-ttu-id="7ea45-139">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7ea45-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="7ea45-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea45-140">System.String</span></span>

## <span data-ttu-id="7ea45-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ea45-141">OUTPUTS</span></span>

### <span data-ttu-id="7ea45-142">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7ea45-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7ea45-143">Note</span><span class="sxs-lookup"><span data-stu-id="7ea45-143">NOTES</span></span>

## <span data-ttu-id="7ea45-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ea45-144">RELATED LINKS</span></span>
