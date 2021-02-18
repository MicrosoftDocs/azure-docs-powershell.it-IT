---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202459"
---
# <span data-ttu-id="e402c-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="e402c-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="e402c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e402c-102">SYNOPSIS</span></span>
<span data-ttu-id="e402c-103">Salva una ipAllocation modificata.</span><span class="sxs-lookup"><span data-stu-id="e402c-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="e402c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e402c-104">SYNTAX</span></span>

### <span data-ttu-id="e402c-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e402c-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e402c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e402c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e402c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e402c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e402c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e402c-108">DESCRIPTION</span></span>
<span data-ttu-id="e402c-109">Il cmdlet **Set-AzIpAllocation** aggiorna una ipAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="e402c-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="e402c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e402c-110">EXAMPLES</span></span>

### <span data-ttu-id="e402c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e402c-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="e402c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e402c-112">PARAMETERS</span></span>

### <span data-ttu-id="e402c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e402c-113">-AsJob</span></span>
<span data-ttu-id="e402c-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e402c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e402c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e402c-115">-DefaultProfile</span></span>
<span data-ttu-id="e402c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e402c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e402c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e402c-117">-InputObject</span></span>
<span data-ttu-id="e402c-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="e402c-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e402c-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="e402c-119">-IpAllocationTag</span></span>
<span data-ttu-id="e402c-120">Tag di allocazione dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="e402c-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e402c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e402c-121">-Name</span></span>
<span data-ttu-id="e402c-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e402c-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e402c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e402c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e402c-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e402c-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e402c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e402c-125">-ResourceId</span></span>
<span data-ttu-id="e402c-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="e402c-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e402c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e402c-127">-Tag</span></span>
<span data-ttu-id="e402c-128">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e402c-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e402c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e402c-129">CommonParameters</span></span>
<span data-ttu-id="e402c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e402c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e402c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e402c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e402c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e402c-132">INPUTS</span></span>

### <span data-ttu-id="e402c-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="e402c-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="e402c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e402c-134">OUTPUTS</span></span>

### <span data-ttu-id="e402c-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="e402c-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="e402c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e402c-136">NOTES</span></span>

## <span data-ttu-id="e402c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e402c-137">RELATED LINKS</span></span>
