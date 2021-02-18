---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206346"
---
# <span data-ttu-id="b47be-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="b47be-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="b47be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b47be-102">SYNOPSIS</span></span>
<span data-ttu-id="b47be-103">Ottenere un elenco di oggetti servizio di peering di un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b47be-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="b47be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b47be-104">SYNTAX</span></span>

### <span data-ttu-id="b47be-105">ByResourceGroupName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b47be-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b47be-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="b47be-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b47be-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b47be-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b47be-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b47be-108">DESCRIPTION</span></span>
<span data-ttu-id="b47be-109">Ottiene servizi di peering per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="b47be-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="b47be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b47be-110">EXAMPLES</span></span>

### <span data-ttu-id="b47be-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b47be-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="b47be-112">Ottiene un servizio di peering per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b47be-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="b47be-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b47be-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="b47be-114">Ottiene un servizio di peering per un gruppo di risorse e il nome</span><span class="sxs-lookup"><span data-stu-id="b47be-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="b47be-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b47be-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="b47be-116">Ottiene un servizio di peering in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b47be-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="b47be-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b47be-117">PARAMETERS</span></span>

### <span data-ttu-id="b47be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47be-118">-DefaultProfile</span></span>
<span data-ttu-id="b47be-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b47be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b47be-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b47be-120">-Name</span></span>
<span data-ttu-id="b47be-121">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="b47be-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b47be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47be-122">-ResourceGroupName</span></span>
<span data-ttu-id="b47be-123">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b47be-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="b47be-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b47be-124">-ResourceId</span></span>
<span data-ttu-id="b47be-125">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b47be-125">The resource id string name.</span></span>

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

### <span data-ttu-id="b47be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47be-126">CommonParameters</span></span>
<span data-ttu-id="b47be-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47be-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b47be-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47be-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="b47be-129">INPUTS</span></span>

### <span data-ttu-id="b47be-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b47be-130">System.String</span></span>

## <span data-ttu-id="b47be-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b47be-131">OUTPUTS</span></span>

### <span data-ttu-id="b47be-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService</span><span class="sxs-lookup"><span data-stu-id="b47be-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="b47be-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="b47be-133">NOTES</span></span>

## <span data-ttu-id="b47be-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b47be-134">RELATED LINKS</span></span>
