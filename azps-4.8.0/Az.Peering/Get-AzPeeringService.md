---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190895"
---
# <span data-ttu-id="1a563-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="1a563-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="1a563-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a563-102">SYNOPSIS</span></span>
<span data-ttu-id="1a563-103">Ottenere un elenco di oggetti del servizio peer di un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a563-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="1a563-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a563-104">SYNTAX</span></span>

### <span data-ttu-id="1a563-105">ByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a563-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a563-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="1a563-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a563-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a563-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a563-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a563-108">DESCRIPTION</span></span>
<span data-ttu-id="1a563-109">Ottiene i servizi di peering per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="1a563-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="1a563-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a563-110">EXAMPLES</span></span>

### <span data-ttu-id="1a563-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a563-111">Example 1</span></span>
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

<span data-ttu-id="1a563-112">Ottiene un servizio peering per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1a563-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="1a563-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1a563-113">Example 2</span></span>
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

<span data-ttu-id="1a563-114">Ottiene un servizio peering per un gruppo di risorse e un nome</span><span class="sxs-lookup"><span data-stu-id="1a563-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="1a563-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1a563-115">Example 3</span></span>
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

<span data-ttu-id="1a563-116">Ottiene un servizio peering tramite ID risorsa</span><span class="sxs-lookup"><span data-stu-id="1a563-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="1a563-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a563-117">PARAMETERS</span></span>

### <span data-ttu-id="1a563-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a563-118">-DefaultProfile</span></span>
<span data-ttu-id="1a563-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a563-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a563-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a563-120">-Name</span></span>
<span data-ttu-id="1a563-121">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1a563-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1a563-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a563-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a563-123">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="1a563-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1a563-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a563-124">-ResourceId</span></span>
<span data-ttu-id="1a563-125">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a563-125">The resource id string name.</span></span>

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

### <span data-ttu-id="1a563-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a563-126">CommonParameters</span></span>
<span data-ttu-id="1a563-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a563-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a563-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a563-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a563-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a563-129">INPUTS</span></span>

### <span data-ttu-id="1a563-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1a563-130">System.String</span></span>

## <span data-ttu-id="1a563-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a563-131">OUTPUTS</span></span>

### <span data-ttu-id="1a563-132">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="1a563-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="1a563-133">Note</span><span class="sxs-lookup"><span data-stu-id="1a563-133">NOTES</span></span>

## <span data-ttu-id="1a563-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a563-134">RELATED LINKS</span></span>