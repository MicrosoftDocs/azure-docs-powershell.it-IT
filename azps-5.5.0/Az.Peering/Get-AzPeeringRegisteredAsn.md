---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202287"
---
# <span data-ttu-id="954b7-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="954b7-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="954b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="954b7-102">SYNOPSIS</span></span>
<span data-ttu-id="954b7-103">Ottiene l'ASN registrato per i peering di tipo Server route Internet.</span><span class="sxs-lookup"><span data-stu-id="954b7-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="954b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="954b7-104">SYNTAX</span></span>

### <span data-ttu-id="954b7-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="954b7-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="954b7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="954b7-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="954b7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="954b7-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="954b7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="954b7-108">DESCRIPTION</span></span>
<span data-ttu-id="954b7-109">Ottenere o elencare un file ASN registrato.</span><span class="sxs-lookup"><span data-stu-id="954b7-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="954b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="954b7-110">EXAMPLES</span></span>

### <span data-ttu-id="954b7-111">Elenco di NOMI registrati per il peering</span><span class="sxs-lookup"><span data-stu-id="954b7-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="954b7-112">Elenchi registrati comen.</span><span class="sxs-lookup"><span data-stu-id="954b7-112">Lists registered asn.</span></span>

### <span data-ttu-id="954b7-113">Viene registrato ASN per il peering in base al nome</span><span class="sxs-lookup"><span data-stu-id="954b7-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="954b7-114">Ottiene l'asn di peering registrato.</span><span class="sxs-lookup"><span data-stu-id="954b7-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="954b7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="954b7-115">PARAMETERS</span></span>

### <span data-ttu-id="954b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954b7-116">-DefaultProfile</span></span>
<span data-ttu-id="954b7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="954b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="954b7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="954b7-118">-InputObject</span></span>
<span data-ttu-id="954b7-119">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="954b7-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="954b7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="954b7-120">-Name</span></span>
<span data-ttu-id="954b7-121">Nome dell'ASN registrato</span><span class="sxs-lookup"><span data-stu-id="954b7-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="954b7-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="954b7-122">-PeeringName</span></span>
<span data-ttu-id="954b7-123">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="954b7-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="954b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="954b7-125">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="954b7-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="954b7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="954b7-126">-ResourceId</span></span>
<span data-ttu-id="954b7-127">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="954b7-127">The resource id string name.</span></span>

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

### <span data-ttu-id="954b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954b7-128">CommonParameters</span></span>
<span data-ttu-id="954b7-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="954b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954b7-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="954b7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954b7-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="954b7-131">INPUTS</span></span>

### <span data-ttu-id="954b7-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSApplicationing</span><span class="sxs-lookup"><span data-stu-id="954b7-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="954b7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="954b7-133">System.String</span></span>

## <span data-ttu-id="954b7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="954b7-134">OUTPUTS</span></span>

### <span data-ttu-id="954b7-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="954b7-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="954b7-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="954b7-136">NOTES</span></span>

## <span data-ttu-id="954b7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="954b7-137">RELATED LINKS</span></span>
