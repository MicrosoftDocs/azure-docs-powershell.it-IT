---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192257"
---
# <span data-ttu-id="71736-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="71736-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="71736-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71736-102">SYNOPSIS</span></span>
<span data-ttu-id="71736-103">Elenca le route ricevute per un peering.</span><span class="sxs-lookup"><span data-stu-id="71736-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="71736-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71736-104">SYNTAX</span></span>

### <span data-ttu-id="71736-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71736-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71736-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71736-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71736-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71736-107">DESCRIPTION</span></span>
<span data-ttu-id="71736-108">Elenca le route ricevute da un peering</span><span class="sxs-lookup"><span data-stu-id="71736-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="71736-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71736-109">EXAMPLES</span></span>

### <span data-ttu-id="71736-110">Elencare le prime 100 Route ricevute per un peering</span><span class="sxs-lookup"><span data-stu-id="71736-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="71736-111">Elenca tutte le route ricevute per un peering</span><span class="sxs-lookup"><span data-stu-id="71736-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="71736-112">Filtrare in base al percorso</span><span class="sxs-lookup"><span data-stu-id="71736-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="71736-113">Elenca tutte le route ricevute per un peering con un filtro attivato come</span><span class="sxs-lookup"><span data-stu-id="71736-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="71736-114">Filtrare per RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="71736-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="71736-115">Elenca tutte le route ricevute per un peering con un filtro in RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="71736-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="71736-116">Filtrare per OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="71736-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="71736-117">Elenca tutte le route ricevute per un peering con un filtro in OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="71736-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="71736-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71736-118">PARAMETERS</span></span>

### <span data-ttu-id="71736-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="71736-119">-AsPath</span></span>
<span data-ttu-id="71736-120">Filtrare in base al percorso.</span><span class="sxs-lookup"><span data-stu-id="71736-120">Filter by AS Path.</span></span>
<span data-ttu-id="71736-121">Esempio:' 9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="71736-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="71736-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71736-122">-DefaultProfile</span></span>
<span data-ttu-id="71736-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71736-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71736-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="71736-124">-Name</span></span>
<span data-ttu-id="71736-125">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="71736-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="71736-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="71736-126">-OriginAsValidationState</span></span>
<span data-ttu-id="71736-127">Filtrare in base all'origine come stato di convalida.</span><span class="sxs-lookup"><span data-stu-id="71736-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="71736-128">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="71736-128">-Prefix</span></span>
<span data-ttu-id="71736-129">Filtrare in base al prefisso.</span><span class="sxs-lookup"><span data-stu-id="71736-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="71736-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71736-130">-ResourceGroupName</span></span>
<span data-ttu-id="71736-131">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="71736-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="71736-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71736-132">-ResourceId</span></span>
<span data-ttu-id="71736-133">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="71736-133">The resource id string name.</span></span>

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

### <span data-ttu-id="71736-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="71736-134">-RPKIValidationState</span></span>
<span data-ttu-id="71736-135">Filtrare in base allo stato di convalida di RPKI.</span><span class="sxs-lookup"><span data-stu-id="71736-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="71736-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71736-136">CommonParameters</span></span>
<span data-ttu-id="71736-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71736-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71736-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71736-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71736-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71736-139">INPUTS</span></span>

### <span data-ttu-id="71736-140">System. String</span><span class="sxs-lookup"><span data-stu-id="71736-140">System.String</span></span>

## <span data-ttu-id="71736-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71736-141">OUTPUTS</span></span>

### <span data-ttu-id="71736-142">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="71736-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="71736-143">Note</span><span class="sxs-lookup"><span data-stu-id="71736-143">NOTES</span></span>

## <span data-ttu-id="71736-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71736-144">RELATED LINKS</span></span>