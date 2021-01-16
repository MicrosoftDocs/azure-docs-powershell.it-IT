---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385262"
---
# <span data-ttu-id="462af-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="462af-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="462af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="462af-102">SYNOPSIS</span></span>
<span data-ttu-id="462af-103">Eliminare una risorsa della tabella route hub virtuale associata a un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="462af-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="462af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="462af-104">SYNTAX</span></span>

### <span data-ttu-id="462af-105">ByVirtualHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="462af-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462af-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="462af-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462af-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="462af-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462af-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="462af-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462af-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="462af-109">DESCRIPTION</span></span>
<span data-ttu-id="462af-110">Elimina la tabella route specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="462af-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="462af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="462af-111">EXAMPLES</span></span>

### <span data-ttu-id="462af-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="462af-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="462af-113">Questo comando Elimina il routeTable1 dell'hub virtuale westushub.</span><span class="sxs-lookup"><span data-stu-id="462af-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="462af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="462af-114">PARAMETERS</span></span>

### <span data-ttu-id="462af-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="462af-115">-AsJob</span></span>
<span data-ttu-id="462af-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="462af-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="462af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462af-117">-DefaultProfile</span></span>
<span data-ttu-id="462af-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="462af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="462af-119">-Force</span><span class="sxs-lookup"><span data-stu-id="462af-119">-Force</span></span>
<span data-ttu-id="462af-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="462af-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="462af-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="462af-121">-HubName</span></span>
<span data-ttu-id="462af-122">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="462af-122">The parent resource name.</span></span>

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

### <span data-ttu-id="462af-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="462af-123">-InputObject</span></span>
<span data-ttu-id="462af-124">La risorsa virtualhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="462af-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="462af-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="462af-125">-Name</span></span>
<span data-ttu-id="462af-126">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="462af-126">The resource name.</span></span>

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

### <span data-ttu-id="462af-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="462af-127">-PassThru</span></span>
<span data-ttu-id="462af-128">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="462af-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="462af-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462af-129">-ResourceGroupName</span></span>
<span data-ttu-id="462af-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="462af-130">The resource group name.</span></span>

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

### <span data-ttu-id="462af-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="462af-131">-ResourceId</span></span>
<span data-ttu-id="462af-132">ID risorsa della risorsa virtualhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="462af-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="462af-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="462af-133">-VirtualHub</span></span>
<span data-ttu-id="462af-134">{{Fill VirtualHub Description}}</span><span class="sxs-lookup"><span data-stu-id="462af-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="462af-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="462af-135">-Confirm</span></span>
<span data-ttu-id="462af-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="462af-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462af-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462af-137">-WhatIf</span></span>
<span data-ttu-id="462af-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="462af-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462af-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="462af-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462af-140">CommonParameters</span></span>
<span data-ttu-id="462af-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="462af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462af-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="462af-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462af-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="462af-143">INPUTS</span></span>

### <span data-ttu-id="462af-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="462af-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="462af-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="462af-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="462af-146">System. String</span><span class="sxs-lookup"><span data-stu-id="462af-146">System.String</span></span>

## <span data-ttu-id="462af-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="462af-147">OUTPUTS</span></span>

### <span data-ttu-id="462af-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="462af-148">System.Boolean</span></span>

## <span data-ttu-id="462af-149">Note</span><span class="sxs-lookup"><span data-stu-id="462af-149">NOTES</span></span>

## <span data-ttu-id="462af-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="462af-150">RELATED LINKS</span></span>
