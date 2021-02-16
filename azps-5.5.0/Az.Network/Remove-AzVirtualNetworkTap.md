---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179454"
---
# <span data-ttu-id="d0b61-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d0b61-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="d0b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b61-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b61-103">Rimuove un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d0b61-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="d0b61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0b61-104">SYNTAX</span></span>

### <span data-ttu-id="d0b61-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0b61-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b61-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b61-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b61-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b61-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b61-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0b61-108">DESCRIPTION</span></span>
<span data-ttu-id="d0b61-109">Il cmdlet **Remove-AzVirtualNetworkTap** rimuove un tocco di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b61-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="d0b61-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0b61-110">EXAMPLES</span></span>

### <span data-ttu-id="d0b61-111">Esempio 1: Rimuovere un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d0b61-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d0b61-112">Questo comando rimuove VirtualNetworkTap1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d0b61-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d0b61-113">Poiché il *parametro Force* non viene usato, all'utente verrà chiesto di confermare l'azione.</span><span class="sxs-lookup"><span data-stu-id="d0b61-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="d0b61-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0b61-114">PARAMETERS</span></span>

### <span data-ttu-id="d0b61-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0b61-115">-AsJob</span></span>
<span data-ttu-id="d0b61-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d0b61-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0b61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b61-117">-DefaultProfile</span></span>
<span data-ttu-id="d0b61-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b61-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d0b61-119">-Force</span></span>
<span data-ttu-id="d0b61-120">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="d0b61-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="d0b61-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0b61-121">-InputObject</span></span>
<span data-ttu-id="d0b61-122">Riferimento alla risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d0b61-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b61-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d0b61-123">-Name</span></span>
<span data-ttu-id="d0b61-124">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="d0b61-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b61-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0b61-125">-PassThru</span></span>
<span data-ttu-id="d0b61-126">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d0b61-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0b61-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d0b61-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0b61-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b61-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0b61-129">Il nome del gruppo di risorse del tocco della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d0b61-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b61-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0b61-130">-ResourceId</span></span>
<span data-ttu-id="d0b61-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="d0b61-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b61-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0b61-132">-Confirm</span></span>
<span data-ttu-id="d0b61-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b61-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b61-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b61-134">-WhatIf</span></span>
<span data-ttu-id="d0b61-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0b61-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b61-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0b61-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b61-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b61-137">CommonParameters</span></span>
<span data-ttu-id="d0b61-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b61-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b61-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b61-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b61-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0b61-140">INPUTS</span></span>

### <span data-ttu-id="d0b61-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d0b61-141">System.String</span></span>

### <span data-ttu-id="d0b61-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d0b61-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d0b61-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0b61-143">OUTPUTS</span></span>

### <span data-ttu-id="d0b61-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0b61-144">System.Boolean</span></span>

## <span data-ttu-id="d0b61-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0b61-145">NOTES</span></span>

## <span data-ttu-id="d0b61-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0b61-146">RELATED LINKS</span></span>

[<span data-ttu-id="d0b61-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d0b61-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="d0b61-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d0b61-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="d0b61-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d0b61-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
