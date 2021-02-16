---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184047"
---
# <span data-ttu-id="5b60f-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="5b60f-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="5b60f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b60f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b60f-103">Elenca le route ricevute per un peering.</span><span class="sxs-lookup"><span data-stu-id="5b60f-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="5b60f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b60f-104">SYNTAX</span></span>

### <span data-ttu-id="5b60f-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b60f-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b60f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b60f-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b60f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5b60f-107">DESCRIPTION</span></span>
<span data-ttu-id="5b60f-108">Elenca le route ricevute da un peering</span><span class="sxs-lookup"><span data-stu-id="5b60f-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="5b60f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b60f-109">EXAMPLES</span></span>

### <span data-ttu-id="5b60f-110">Elencare le prime 100 route ricevute per un peering</span><span class="sxs-lookup"><span data-stu-id="5b60f-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="5b60f-111">Elenca tutte le route ricevute per un peering</span><span class="sxs-lookup"><span data-stu-id="5b60f-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="5b60f-112">Filtrare in base al percorso AS</span><span class="sxs-lookup"><span data-stu-id="5b60f-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="5b60f-113">Elenca tutte le route ricevute per un peering con un filtro su AS</span><span class="sxs-lookup"><span data-stu-id="5b60f-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="5b60f-114">Filtrare in base a RPKIValidState</span><span class="sxs-lookup"><span data-stu-id="5b60f-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="5b60f-115">Elenca tutte le route ricevute per un peering con un filtro in RPKIValidState</span><span class="sxs-lookup"><span data-stu-id="5b60f-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="5b60f-116">Filtrare in base a OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="5b60f-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="5b60f-117">Elenca tutte le route ricevute per un peering con un filtro in OriginAsValidState</span><span class="sxs-lookup"><span data-stu-id="5b60f-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="5b60f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b60f-118">PARAMETERS</span></span>

### <span data-ttu-id="5b60f-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="5b60f-119">-AsPath</span></span>
<span data-ttu-id="5b60f-120">Filtrare in base al percorso AS.</span><span class="sxs-lookup"><span data-stu-id="5b60f-120">Filter by AS Path.</span></span>
<span data-ttu-id="5b60f-121">Esempio: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="5b60f-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="5b60f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b60f-122">-DefaultProfile</span></span>
<span data-ttu-id="5b60f-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b60f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b60f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5b60f-124">-Name</span></span>
<span data-ttu-id="5b60f-125">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="5b60f-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b60f-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="5b60f-126">-OriginAsValidationState</span></span>
<span data-ttu-id="5b60f-127">Filtrare in base allo stato di convalida ORIGIN AS.</span><span class="sxs-lookup"><span data-stu-id="5b60f-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="5b60f-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5b60f-128">-Prefix</span></span>
<span data-ttu-id="5b60f-129">Filtrare in base al prefisso.</span><span class="sxs-lookup"><span data-stu-id="5b60f-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="5b60f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b60f-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b60f-131">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="5b60f-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="5b60f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b60f-132">-ResourceId</span></span>
<span data-ttu-id="5b60f-133">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b60f-133">The resource id string name.</span></span>

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

### <span data-ttu-id="5b60f-134">-RPKIValidState</span><span class="sxs-lookup"><span data-stu-id="5b60f-134">-RPKIValidationState</span></span>
<span data-ttu-id="5b60f-135">Filtrare in base allo stato di convalida RPKI.</span><span class="sxs-lookup"><span data-stu-id="5b60f-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="5b60f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b60f-136">CommonParameters</span></span>
<span data-ttu-id="5b60f-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b60f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b60f-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b60f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b60f-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="5b60f-139">INPUTS</span></span>

### <span data-ttu-id="5b60f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5b60f-140">System.String</span></span>

## <span data-ttu-id="5b60f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b60f-141">OUTPUTS</span></span>

### <span data-ttu-id="5b60f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSApplicationingReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="5b60f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="5b60f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="5b60f-143">NOTES</span></span>

## <span data-ttu-id="5b60f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b60f-144">RELATED LINKS</span></span>
