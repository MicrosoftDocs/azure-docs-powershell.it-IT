---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179415"
---
# <span data-ttu-id="3e805-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3e805-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="3e805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e805-102">SYNOPSIS</span></span>
<span data-ttu-id="3e805-103">Rimuove una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e805-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="3e805-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e805-104">SYNTAX</span></span>

### <span data-ttu-id="3e805-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e805-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e805-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="3e805-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e805-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="3e805-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e805-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e805-108">DESCRIPTION</span></span>
<span data-ttu-id="3e805-109">Rimuove una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e805-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="3e805-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e805-110">EXAMPLES</span></span>

### <span data-ttu-id="3e805-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e805-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="3e805-112">Questo esempio crea una WAN virtuale in un gruppo di risorse e quindi la elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3e805-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3e805-113">Per eliminare la richiesta quando si elimina la WAN virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="3e805-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="3e805-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e805-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="3e805-115">Questo esempio crea una WAN virtuale in un gruppo di risorse e quindi la elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3e805-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3e805-116">Questa eliminazione si verifica usando l'oggetto Wan virtuale restituito da New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="3e805-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="3e805-117">Per eliminare la richiesta quando si elimina la WAN virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="3e805-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="3e805-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3e805-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="3e805-119">Questo esempio crea una WAN virtuale in un gruppo di risorse e quindi la elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3e805-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3e805-120">Questa eliminazione si verifica usando l'ID risorsa WAN virtuale restituito da New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="3e805-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="3e805-121">Per eliminare la richiesta quando si elimina la WAN virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="3e805-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="3e805-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e805-122">PARAMETERS</span></span>

### <span data-ttu-id="3e805-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e805-123">-DefaultProfile</span></span>
<span data-ttu-id="3e805-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e805-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e805-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3e805-125">-Force</span></span>
<span data-ttu-id="3e805-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3e805-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e805-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e805-127">-InputObject</span></span>
<span data-ttu-id="3e805-128">L'oggetto Wan virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3e805-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e805-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3e805-129">-Name</span></span>
<span data-ttu-id="3e805-130">Nome WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e805-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e805-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e805-131">-PassThru</span></span>
<span data-ttu-id="3e805-132">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3e805-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e805-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3e805-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e805-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e805-134">-ResourceGroupName</span></span>
<span data-ttu-id="3e805-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e805-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e805-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e805-136">-ResourceId</span></span>
<span data-ttu-id="3e805-137">ID della risorsa Azure per la wan virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3e805-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e805-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e805-138">-Confirm</span></span>
<span data-ttu-id="3e805-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e805-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e805-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e805-140">-WhatIf</span></span>
<span data-ttu-id="3e805-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e805-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e805-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e805-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e805-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e805-143">CommonParameters</span></span>
<span data-ttu-id="3e805-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e805-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e805-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e805-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e805-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e805-146">INPUTS</span></span>

### <span data-ttu-id="3e805-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3e805-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="3e805-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3e805-148">System.String</span></span>

## <span data-ttu-id="3e805-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e805-149">OUTPUTS</span></span>

### <span data-ttu-id="3e805-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e805-150">System.Boolean</span></span>

## <span data-ttu-id="3e805-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e805-151">NOTES</span></span>

## <span data-ttu-id="3e805-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e805-152">RELATED LINKS</span></span>

[<span data-ttu-id="3e805-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3e805-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="3e805-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3e805-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="3e805-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3e805-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
