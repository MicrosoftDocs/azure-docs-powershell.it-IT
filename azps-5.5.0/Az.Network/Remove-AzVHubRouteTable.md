---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193455"
---
# <span data-ttu-id="be8b7-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="be8b7-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="be8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="be8b7-103">Eliminare una risorsa tabella delle route dell'hub associata a un virtualhub.</span><span class="sxs-lookup"><span data-stu-id="be8b7-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="be8b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be8b7-104">SYNTAX</span></span>

### <span data-ttu-id="be8b7-105">ByVHubRouteTableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be8b7-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8b7-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="be8b7-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8b7-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="be8b7-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8b7-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="be8b7-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be8b7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be8b7-109">DESCRIPTION</span></span>
<span data-ttu-id="be8b7-110">Elimina la tabella delle route dell'hub specificata associata all'hub virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="be8b7-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="be8b7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be8b7-111">EXAMPLES</span></span>

### <span data-ttu-id="be8b7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be8b7-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="be8b7-113">Questo comando elimina la tabella delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="be8b7-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="be8b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be8b7-114">PARAMETERS</span></span>

### <span data-ttu-id="be8b7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be8b7-115">-AsJob</span></span>
<span data-ttu-id="be8b7-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="be8b7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be8b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8b7-117">-DefaultProfile</span></span>
<span data-ttu-id="be8b7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be8b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be8b7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="be8b7-119">-Force</span></span>
<span data-ttu-id="be8b7-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="be8b7-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="be8b7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be8b7-121">-InputObject</span></span>
<span data-ttu-id="be8b7-122">La risorsa vhubroute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="be8b7-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="be8b7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="be8b7-123">-Name</span></span>
<span data-ttu-id="be8b7-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be8b7-124">The resource name.</span></span>

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

### <span data-ttu-id="be8b7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="be8b7-125">-ParentObject</span></span>
<span data-ttu-id="be8b7-126">Oggetto hub virtuale padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be8b7-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="be8b7-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="be8b7-127">-ParentResourceName</span></span>
<span data-ttu-id="be8b7-128">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="be8b7-128">The parent resource name.</span></span>

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

### <span data-ttu-id="be8b7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be8b7-129">-PassThru</span></span>
<span data-ttu-id="be8b7-130">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="be8b7-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="be8b7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be8b7-131">-ResourceGroupName</span></span>
<span data-ttu-id="be8b7-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="be8b7-132">The resource group name.</span></span>

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

### <span data-ttu-id="be8b7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be8b7-133">-ResourceId</span></span>
<span data-ttu-id="be8b7-134">ID della risorsa vhubroutetable da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="be8b7-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="be8b7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be8b7-135">-Confirm</span></span>
<span data-ttu-id="be8b7-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be8b7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8b7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8b7-137">-WhatIf</span></span>
<span data-ttu-id="be8b7-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be8b7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be8b7-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be8b7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8b7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8b7-140">CommonParameters</span></span>
<span data-ttu-id="be8b7-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be8b7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8b7-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be8b7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8b7-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="be8b7-143">INPUTS</span></span>

### <span data-ttu-id="be8b7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="be8b7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="be8b7-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="be8b7-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="be8b7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="be8b7-146">System.String</span></span>

## <span data-ttu-id="be8b7-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be8b7-147">OUTPUTS</span></span>

### <span data-ttu-id="be8b7-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be8b7-148">System.Boolean</span></span>

## <span data-ttu-id="be8b7-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="be8b7-149">NOTES</span></span>

## <span data-ttu-id="be8b7-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be8b7-150">RELATED LINKS</span></span>

[<span data-ttu-id="be8b7-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="be8b7-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="be8b7-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="be8b7-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="be8b7-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="be8b7-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="be8b7-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="be8b7-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)