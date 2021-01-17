---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488944"
---
# <span data-ttu-id="eb585-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb585-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="eb585-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb585-102">SYNOPSIS</span></span>
<span data-ttu-id="eb585-103">Eliminare una risorsa della tabella route Hub associata a un VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="eb585-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="eb585-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb585-104">SYNTAX</span></span>

### <span data-ttu-id="eb585-105">ByVHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb585-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb585-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="eb585-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb585-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="eb585-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb585-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="eb585-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb585-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb585-109">DESCRIPTION</span></span>
<span data-ttu-id="eb585-110">Elimina la tabella route Hub specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="eb585-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="eb585-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb585-111">EXAMPLES</span></span>

### <span data-ttu-id="eb585-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb585-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="eb585-113">Questo comando Elimina la tabella route Hub dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb585-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="eb585-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb585-114">PARAMETERS</span></span>

### <span data-ttu-id="eb585-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb585-115">-AsJob</span></span>
<span data-ttu-id="eb585-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eb585-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb585-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb585-117">-DefaultProfile</span></span>
<span data-ttu-id="eb585-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb585-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb585-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eb585-119">-Force</span></span>
<span data-ttu-id="eb585-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="eb585-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eb585-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb585-121">-InputObject</span></span>
<span data-ttu-id="eb585-122">La risorsa vhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="eb585-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb585-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb585-123">-Name</span></span>
<span data-ttu-id="eb585-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb585-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb585-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb585-125">-ParentObject</span></span>
<span data-ttu-id="eb585-126">L'oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb585-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb585-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="eb585-127">-ParentResourceName</span></span>
<span data-ttu-id="eb585-128">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="eb585-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb585-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb585-129">-PassThru</span></span>
<span data-ttu-id="eb585-130">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="eb585-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="eb585-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb585-131">-ResourceGroupName</span></span>
<span data-ttu-id="eb585-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb585-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb585-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb585-133">-ResourceId</span></span>
<span data-ttu-id="eb585-134">ID risorsa della risorsa vhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="eb585-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb585-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb585-135">-Confirm</span></span>
<span data-ttu-id="eb585-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb585-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb585-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb585-137">-WhatIf</span></span>
<span data-ttu-id="eb585-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb585-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb585-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb585-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb585-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb585-140">CommonParameters</span></span>
<span data-ttu-id="eb585-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb585-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb585-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb585-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb585-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb585-143">INPUTS</span></span>

### <span data-ttu-id="eb585-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="eb585-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="eb585-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb585-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="eb585-146">System. String</span><span class="sxs-lookup"><span data-stu-id="eb585-146">System.String</span></span>

## <span data-ttu-id="eb585-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb585-147">OUTPUTS</span></span>

### <span data-ttu-id="eb585-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb585-148">System.Boolean</span></span>

## <span data-ttu-id="eb585-149">Note</span><span class="sxs-lookup"><span data-stu-id="eb585-149">NOTES</span></span>

## <span data-ttu-id="eb585-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb585-150">RELATED LINKS</span></span>

[<span data-ttu-id="eb585-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb585-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="eb585-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="eb585-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="eb585-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb585-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="eb585-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb585-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)