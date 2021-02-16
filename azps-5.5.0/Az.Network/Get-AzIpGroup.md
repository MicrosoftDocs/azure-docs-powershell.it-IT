---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189766"
---
# <span data-ttu-id="79bac-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="79bac-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="79bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79bac-102">SYNOPSIS</span></span>
<span data-ttu-id="79bac-103">Ottenere un IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="79bac-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="79bac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79bac-104">SYNTAX</span></span>

### <span data-ttu-id="79bac-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79bac-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79bac-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79bac-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79bac-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79bac-107">DESCRIPTION</span></span>
<span data-ttu-id="79bac-108">Il **cmdlet Get-AzIpGroup** ottiene un gruppo IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="79bac-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="79bac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79bac-109">EXAMPLES</span></span>

### <span data-ttu-id="79bac-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79bac-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="79bac-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="79bac-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="79bac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79bac-112">PARAMETERS</span></span>

### <span data-ttu-id="79bac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bac-113">-DefaultProfile</span></span>
<span data-ttu-id="79bac-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79bac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79bac-115">-Name</span><span class="sxs-lookup"><span data-stu-id="79bac-115">-Name</span></span>
<span data-ttu-id="79bac-116">Nome del gruppo ipgroup.</span><span class="sxs-lookup"><span data-stu-id="79bac-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="79bac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79bac-117">-ResourceGroupName</span></span>
<span data-ttu-id="79bac-118">Nome del gruppo di risorse dell'ipgroup.</span><span class="sxs-lookup"><span data-stu-id="79bac-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="79bac-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79bac-119">-ResourceId</span></span>
<span data-ttu-id="79bac-120">ResourceId dell'ipgroup.</span><span class="sxs-lookup"><span data-stu-id="79bac-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="79bac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bac-121">CommonParameters</span></span>
<span data-ttu-id="79bac-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bac-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79bac-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bac-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="79bac-124">INPUTS</span></span>

### <span data-ttu-id="79bac-125">System.String</span><span class="sxs-lookup"><span data-stu-id="79bac-125">System.String</span></span>

## <span data-ttu-id="79bac-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79bac-126">OUTPUTS</span></span>

### <span data-ttu-id="79bac-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="79bac-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="79bac-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="79bac-128">NOTES</span></span>

## <span data-ttu-id="79bac-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79bac-129">RELATED LINKS</span></span>
