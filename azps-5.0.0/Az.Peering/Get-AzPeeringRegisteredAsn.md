---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199843"
---
# <span data-ttu-id="f4274-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="f4274-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="f4274-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4274-102">SYNOPSIS</span></span>
<span data-ttu-id="f4274-103">Ottiene l'ASN registrato per i peer del tipo di server route di Exchange per Internet.</span><span class="sxs-lookup"><span data-stu-id="f4274-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="f4274-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4274-104">SYNTAX</span></span>

### <span data-ttu-id="f4274-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4274-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4274-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4274-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4274-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4274-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4274-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4274-108">DESCRIPTION</span></span>
<span data-ttu-id="f4274-109">Ottenere o elencare un ASN registrato.</span><span class="sxs-lookup"><span data-stu-id="f4274-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="f4274-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4274-110">EXAMPLES</span></span>

### <span data-ttu-id="f4274-111">Elenco di ASN registrati per il peering</span><span class="sxs-lookup"><span data-stu-id="f4274-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="f4274-112">Elenca gli elenchi ASN registrati.</span><span class="sxs-lookup"><span data-stu-id="f4274-112">Lists registered asn.</span></span>

### <span data-ttu-id="f4274-113">Ottiene l'ASN registrato per il peering per nome</span><span class="sxs-lookup"><span data-stu-id="f4274-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="f4274-114">Ottiene il peering ASN registrato.</span><span class="sxs-lookup"><span data-stu-id="f4274-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="f4274-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4274-115">PARAMETERS</span></span>

### <span data-ttu-id="f4274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4274-116">-DefaultProfile</span></span>
<span data-ttu-id="f4274-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4274-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4274-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4274-118">-InputObject</span></span>
<span data-ttu-id="f4274-119">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f4274-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4274-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4274-120">-Name</span></span>
<span data-ttu-id="f4274-121">Nome dell'ASN registrato</span><span class="sxs-lookup"><span data-stu-id="f4274-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4274-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="f4274-122">-PeeringName</span></span>
<span data-ttu-id="f4274-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f4274-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f4274-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4274-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4274-125">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="f4274-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f4274-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4274-126">-ResourceId</span></span>
<span data-ttu-id="f4274-127">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4274-127">The resource id string name.</span></span>

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

### <span data-ttu-id="f4274-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4274-128">CommonParameters</span></span>
<span data-ttu-id="f4274-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4274-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4274-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4274-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4274-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4274-131">INPUTS</span></span>

### <span data-ttu-id="f4274-132">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f4274-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="f4274-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f4274-133">System.String</span></span>

## <span data-ttu-id="f4274-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4274-134">OUTPUTS</span></span>

### <span data-ttu-id="f4274-135">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="f4274-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="f4274-136">Note</span><span class="sxs-lookup"><span data-stu-id="f4274-136">NOTES</span></span>

## <span data-ttu-id="f4274-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4274-137">RELATED LINKS</span></span>