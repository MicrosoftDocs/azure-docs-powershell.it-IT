---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372214"
---
# <span data-ttu-id="6fba7-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6fba7-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="6fba7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fba7-102">SYNOPSIS</span></span>
<span data-ttu-id="6fba7-103">Ottenere un Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="6fba7-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="6fba7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fba7-104">SYNTAX</span></span>

### <span data-ttu-id="6fba7-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fba7-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fba7-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fba7-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fba7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fba7-107">DESCRIPTION</span></span>
<span data-ttu-id="6fba7-108">Il cmdlet **Get-AzIpGroup** ottiene un IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="6fba7-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="6fba7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fba7-109">EXAMPLES</span></span>

### <span data-ttu-id="6fba7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fba7-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="6fba7-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6fba7-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="6fba7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fba7-112">PARAMETERS</span></span>

### <span data-ttu-id="6fba7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fba7-113">-DefaultProfile</span></span>
<span data-ttu-id="6fba7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fba7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fba7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fba7-115">-Name</span></span>
<span data-ttu-id="6fba7-116">Il nome del ipgroup.</span><span class="sxs-lookup"><span data-stu-id="6fba7-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fba7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fba7-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fba7-118">Nome del gruppo di risorse di ipgroup.</span><span class="sxs-lookup"><span data-stu-id="6fba7-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fba7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fba7-119">-ResourceId</span></span>
<span data-ttu-id="6fba7-120">ResourceId di ipgroup.</span><span class="sxs-lookup"><span data-stu-id="6fba7-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fba7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fba7-121">CommonParameters</span></span>
<span data-ttu-id="6fba7-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fba7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fba7-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fba7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fba7-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fba7-124">INPUTS</span></span>

### <span data-ttu-id="6fba7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6fba7-125">System.String</span></span>

## <span data-ttu-id="6fba7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fba7-126">OUTPUTS</span></span>

### <span data-ttu-id="6fba7-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="6fba7-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="6fba7-128">Note</span><span class="sxs-lookup"><span data-stu-id="6fba7-128">NOTES</span></span>

## <span data-ttu-id="6fba7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fba7-129">RELATED LINKS</span></span>
