---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206547"
---
# <span data-ttu-id="b5495-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5495-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="b5495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5495-102">SYNOPSIS</span></span>
<span data-ttu-id="b5495-103">Eliminare una risorsa tabella di route dell'hub virtuale associata a un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5495-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="b5495-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5495-104">SYNTAX</span></span>

### <span data-ttu-id="b5495-105">ByVirtualHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5495-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5495-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b5495-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5495-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="b5495-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5495-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="b5495-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5495-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5495-109">DESCRIPTION</span></span>
<span data-ttu-id="b5495-110">Elimina la tabella di route specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="b5495-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="b5495-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5495-111">EXAMPLES</span></span>

### <span data-ttu-id="b5495-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5495-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="b5495-113">Questo comando elimina la routeTable1 dell'hub virtuale westushub.</span><span class="sxs-lookup"><span data-stu-id="b5495-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="b5495-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5495-114">PARAMETERS</span></span>

### <span data-ttu-id="b5495-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5495-115">-AsJob</span></span>
<span data-ttu-id="b5495-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b5495-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5495-117">-DefaultProfile</span></span>
<span data-ttu-id="b5495-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5495-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5495-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b5495-119">-Force</span></span>
<span data-ttu-id="b5495-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="b5495-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="b5495-121">-HubName</span></span>
<span data-ttu-id="b5495-122">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="b5495-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5495-123">-InputObject</span></span>
<span data-ttu-id="b5495-124">La risorsa virtualhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b5495-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b5495-125">-Name</span></span>
<span data-ttu-id="b5495-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5495-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5495-127">-PassThru</span></span>
<span data-ttu-id="b5495-128">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5495-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5495-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5495-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5495-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5495-131">-ResourceId</span></span>
<span data-ttu-id="b5495-132">ID risorsa della risorsa della tabella Virtualhubroute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b5495-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b5495-133">-VirtualHub</span></span>
<span data-ttu-id="b5495-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="b5495-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5495-135">-Confirm</span></span>
<span data-ttu-id="b5495-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5495-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5495-137">-WhatIf</span></span>
<span data-ttu-id="b5495-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5495-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5495-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5495-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5495-140">CommonParameters</span></span>
<span data-ttu-id="b5495-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5495-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5495-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5495-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5495-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5495-143">INPUTS</span></span>

### <span data-ttu-id="b5495-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b5495-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b5495-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5495-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="b5495-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b5495-146">System.String</span></span>

## <span data-ttu-id="b5495-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5495-147">OUTPUTS</span></span>

### <span data-ttu-id="b5495-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5495-148">System.Boolean</span></span>

## <span data-ttu-id="b5495-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5495-149">NOTES</span></span>

## <span data-ttu-id="b5495-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5495-150">RELATED LINKS</span></span>
