---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
ms.openlocfilehash: 1ff9eb4307c4419dd303d74f7528a8ee0d50bdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513607"
---
# <span data-ttu-id="5cf1e-101">Remove-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5cf1e-101">Remove-AzureRmVirtualWan</span></span>

## <span data-ttu-id="5cf1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cf1e-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf1e-103">Rimuove una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-103">Removes an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cf1e-104">SYNTAX</span></span>

### <span data-ttu-id="5cf1e-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cf1e-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf1e-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="5cf1e-106">ByVirtualWanObject</span></span>
```
Remove-AzureRmVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf1e-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf1e-107">ByVirtualWanResourceId</span></span>
```
Remove-AzureRmVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf1e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cf1e-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf1e-109">Rimuove una WAN virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="5cf1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cf1e-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf1e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5cf1e-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="5cf1e-112">Questo esempio crea una WAN virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="5cf1e-113">Per eliminare la richiesta quando si elimina la rete WAN virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="5cf1e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5cf1e-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="5cf1e-115">Questo esempio crea una WAN virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="5cf1e-116">Questa operazione viene eseguita usando l'oggetto WAN virtuale restituito da New-AzureRmVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-116">This deletion happens using the virtual wan object returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="5cf1e-117">Per eliminare la richiesta quando si elimina la rete WAN virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="5cf1e-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5cf1e-118">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="5cf1e-119">Questo esempio crea una WAN virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="5cf1e-120">Questa operazione viene eseguita usando l'ID risorsa WAN virtuale restituito da New-AzureRmVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-120">This deletion happens using the virtual wan resource id returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="5cf1e-121">Per eliminare la richiesta quando si elimina la rete WAN virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="5cf1e-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cf1e-122">PARAMETERS</span></span>

### <span data-ttu-id="5cf1e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf1e-123">-DefaultProfile</span></span>
<span data-ttu-id="5cf1e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf1e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5cf1e-125">-Force</span></span>
<span data-ttu-id="5cf1e-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5cf1e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cf1e-127">-InputObject</span></span>
<span data-ttu-id="5cf1e-128">L'oggetto WAN virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="5cf1e-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cf1e-129">-Name</span></span>
<span data-ttu-id="5cf1e-130">Nome della rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="5cf1e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cf1e-131">-PassThru</span></span>
<span data-ttu-id="5cf1e-132">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5cf1e-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5cf1e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf1e-134">-ResourceGroupName</span></span>
<span data-ttu-id="5cf1e-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-135">The resource group name.</span></span>

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

### <span data-ttu-id="5cf1e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf1e-136">-ResourceId</span></span>
<span data-ttu-id="5cf1e-137">ID risorsa Azure per la rete WAN virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="5cf1e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5cf1e-138">-Confirm</span></span>
<span data-ttu-id="5cf1e-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf1e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf1e-140">-WhatIf</span></span>
<span data-ttu-id="5cf1e-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf1e-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf1e-143">CommonParameters</span></span>
<span data-ttu-id="5cf1e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf1e-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf1e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf1e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cf1e-146">INPUTS</span></span>

### <span data-ttu-id="5cf1e-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="5cf1e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="5cf1e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf1e-148">System.String</span></span>

## <span data-ttu-id="5cf1e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cf1e-149">OUTPUTS</span></span>

### <span data-ttu-id="5cf1e-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5cf1e-150">System.Boolean</span></span>

## <span data-ttu-id="5cf1e-151">Note</span><span class="sxs-lookup"><span data-stu-id="5cf1e-151">NOTES</span></span>

## <span data-ttu-id="5cf1e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cf1e-152">RELATED LINKS</span></span>
