---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201564"
---
# <span data-ttu-id="26adc-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="26adc-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="26adc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26adc-102">SYNOPSIS</span></span>
<span data-ttu-id="26adc-103">Eliminare una risorsa della tabella route Hub associata a un VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="26adc-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="26adc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26adc-104">SYNTAX</span></span>

### <span data-ttu-id="26adc-105">ByVHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26adc-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26adc-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="26adc-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26adc-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="26adc-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26adc-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="26adc-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26adc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26adc-109">DESCRIPTION</span></span>
<span data-ttu-id="26adc-110">Elimina la tabella route Hub specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="26adc-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="26adc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26adc-111">EXAMPLES</span></span>

### <span data-ttu-id="26adc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26adc-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="26adc-113">Questo comando Elimina la tabella route Hub dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="26adc-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="26adc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26adc-114">PARAMETERS</span></span>

### <span data-ttu-id="26adc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26adc-115">-AsJob</span></span>
<span data-ttu-id="26adc-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="26adc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26adc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26adc-117">-DefaultProfile</span></span>
<span data-ttu-id="26adc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26adc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26adc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="26adc-119">-Force</span></span>
<span data-ttu-id="26adc-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="26adc-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="26adc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26adc-121">-InputObject</span></span>
<span data-ttu-id="26adc-122">La risorsa vhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26adc-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="26adc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="26adc-123">-Name</span></span>
<span data-ttu-id="26adc-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="26adc-124">The resource name.</span></span>

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

### <span data-ttu-id="26adc-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="26adc-125">-ParentObject</span></span>
<span data-ttu-id="26adc-126">L'oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="26adc-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="26adc-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="26adc-127">-ParentResourceName</span></span>
<span data-ttu-id="26adc-128">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="26adc-128">The parent resource name.</span></span>

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

### <span data-ttu-id="26adc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26adc-129">-PassThru</span></span>
<span data-ttu-id="26adc-130">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="26adc-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="26adc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26adc-131">-ResourceGroupName</span></span>
<span data-ttu-id="26adc-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26adc-132">The resource group name.</span></span>

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

### <span data-ttu-id="26adc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26adc-133">-ResourceId</span></span>
<span data-ttu-id="26adc-134">ID risorsa della risorsa vhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26adc-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="26adc-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26adc-135">-Confirm</span></span>
<span data-ttu-id="26adc-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26adc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26adc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26adc-137">-WhatIf</span></span>
<span data-ttu-id="26adc-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26adc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26adc-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26adc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26adc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26adc-140">CommonParameters</span></span>
<span data-ttu-id="26adc-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26adc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26adc-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26adc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26adc-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26adc-143">INPUTS</span></span>

### <span data-ttu-id="26adc-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="26adc-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="26adc-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="26adc-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="26adc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="26adc-146">System.String</span></span>

## <span data-ttu-id="26adc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26adc-147">OUTPUTS</span></span>

### <span data-ttu-id="26adc-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26adc-148">System.Boolean</span></span>

## <span data-ttu-id="26adc-149">Note</span><span class="sxs-lookup"><span data-stu-id="26adc-149">NOTES</span></span>

## <span data-ttu-id="26adc-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26adc-150">RELATED LINKS</span></span>

[<span data-ttu-id="26adc-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="26adc-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="26adc-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="26adc-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="26adc-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="26adc-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="26adc-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="26adc-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)