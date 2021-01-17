---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488909"
---
# <span data-ttu-id="c9156-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c9156-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="c9156-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9156-102">SYNOPSIS</span></span>
<span data-ttu-id="c9156-103">Salva un IpAllocation modificato.</span><span class="sxs-lookup"><span data-stu-id="c9156-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="c9156-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9156-104">SYNTAX</span></span>

### <span data-ttu-id="c9156-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9156-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9156-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9156-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9156-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9156-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9156-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9156-108">DESCRIPTION</span></span>
<span data-ttu-id="c9156-109">Il cmdlet **set-AzIpAllocation** aggiorna un IpAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="c9156-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="c9156-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9156-110">EXAMPLES</span></span>

### <span data-ttu-id="c9156-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9156-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="c9156-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9156-112">PARAMETERS</span></span>

### <span data-ttu-id="c9156-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9156-113">-AsJob</span></span>
<span data-ttu-id="c9156-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c9156-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9156-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9156-115">-DefaultProfile</span></span>
<span data-ttu-id="c9156-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9156-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9156-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9156-117">-InputObject</span></span>
<span data-ttu-id="c9156-118">IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c9156-118">The IpAllocation</span></span>

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

### <span data-ttu-id="c9156-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="c9156-119">-IpAllocationTag</span></span>
<span data-ttu-id="c9156-120">Tag di allocazione dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="c9156-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="c9156-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9156-121">-Name</span></span>
<span data-ttu-id="c9156-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9156-122">The resource name.</span></span>

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

### <span data-ttu-id="c9156-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9156-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9156-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9156-124">The resource group name.</span></span>

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

### <span data-ttu-id="c9156-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9156-125">-ResourceId</span></span>
<span data-ttu-id="c9156-126">ID IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c9156-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="c9156-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9156-127">-Tag</span></span>
<span data-ttu-id="c9156-128">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c9156-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c9156-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9156-129">CommonParameters</span></span>
<span data-ttu-id="c9156-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9156-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9156-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9156-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9156-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9156-132">INPUTS</span></span>

### <span data-ttu-id="c9156-133">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c9156-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="c9156-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9156-134">OUTPUTS</span></span>

### <span data-ttu-id="c9156-135">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c9156-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="c9156-136">Note</span><span class="sxs-lookup"><span data-stu-id="c9156-136">NOTES</span></span>

## <span data-ttu-id="c9156-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9156-137">RELATED LINKS</span></span>
