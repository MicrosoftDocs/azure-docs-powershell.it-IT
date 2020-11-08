---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190890"
---
# <span data-ttu-id="08dd7-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="08dd7-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="08dd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="08dd7-103">Imposta o aggiorna un prefisso registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="08dd7-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="08dd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08dd7-104">SYNTAX</span></span>

### <span data-ttu-id="08dd7-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08dd7-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08dd7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="08dd7-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08dd7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08dd7-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08dd7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08dd7-108">DESCRIPTION</span></span>
<span data-ttu-id="08dd7-109">Consente l'aggiornamento di un prefisso registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="08dd7-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="08dd7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="08dd7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08dd7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="08dd7-112">Aggiorna il prefisso per ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="08dd7-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="08dd7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08dd7-113">PARAMETERS</span></span>

### <span data-ttu-id="08dd7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08dd7-114">-AsJob</span></span>
<span data-ttu-id="08dd7-115">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="08dd7-115">Run in the background.</span></span>

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

### <span data-ttu-id="08dd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08dd7-116">-DefaultProfile</span></span>
<span data-ttu-id="08dd7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08dd7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08dd7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08dd7-118">-InputObject</span></span>
<span data-ttu-id="08dd7-119">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="08dd7-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="08dd7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="08dd7-120">-Name</span></span>
<span data-ttu-id="08dd7-121">Il nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="08dd7-121">The name of prefix.</span></span>

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

### <span data-ttu-id="08dd7-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="08dd7-122">-PeeringName</span></span>
<span data-ttu-id="08dd7-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="08dd7-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="08dd7-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="08dd7-124">-Prefix</span></span>
<span data-ttu-id="08dd7-125">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="08dd7-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="08dd7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08dd7-126">-ResourceGroupName</span></span>
<span data-ttu-id="08dd7-127">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="08dd7-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="08dd7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08dd7-128">-ResourceId</span></span>
<span data-ttu-id="08dd7-129">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="08dd7-129">The resource id string name.</span></span>

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

### <span data-ttu-id="08dd7-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08dd7-130">-Confirm</span></span>
<span data-ttu-id="08dd7-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08dd7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08dd7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08dd7-132">-WhatIf</span></span>
<span data-ttu-id="08dd7-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08dd7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08dd7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08dd7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08dd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08dd7-135">CommonParameters</span></span>
<span data-ttu-id="08dd7-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08dd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08dd7-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08dd7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08dd7-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08dd7-138">INPUTS</span></span>

### <span data-ttu-id="08dd7-139">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="08dd7-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="08dd7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="08dd7-140">System.String</span></span>

## <span data-ttu-id="08dd7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08dd7-141">OUTPUTS</span></span>

### <span data-ttu-id="08dd7-142">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="08dd7-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="08dd7-143">Note</span><span class="sxs-lookup"><span data-stu-id="08dd7-143">NOTES</span></span>

## <span data-ttu-id="08dd7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08dd7-144">RELATED LINKS</span></span>
