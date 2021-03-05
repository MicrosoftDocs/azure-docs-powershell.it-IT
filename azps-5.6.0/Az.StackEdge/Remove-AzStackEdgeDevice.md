---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 174fe29d45d20b1b1e0ed0c3935bfd99ad2e1a87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005182"
---
# <span data-ttu-id="d5f4b-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d5f4b-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="d5f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f4b-103">Rimuove un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="d5f4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5f4b-104">SYNTAX</span></span>

### <span data-ttu-id="d5f4b-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5f4b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5f4b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f4b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5f4b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f4b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5f4b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5f4b-108">DESCRIPTION</span></span>
<span data-ttu-id="d5f4b-109">Il cmdlet **Remove-AzStackEdgeDevice** rimuove la configurazione per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="d5f4b-110">Tieni presente che il dispositivo può essere eliminato solo dopo aver effettuato l'ordine e prima che il dispositivo venga preparato da Microsoft per la spedizione.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="d5f4b-111">Fare riferimento alla documentazione sull'eliminazione della risorsa prima di usare questo [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="d5f4b-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="d5f4b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5f4b-112">EXAMPLES</span></span>

### <span data-ttu-id="d5f4b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5f4b-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="d5f4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5f4b-114">PARAMETERS</span></span>

### <span data-ttu-id="d5f4b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5f4b-115">-AsJob</span></span>
<span data-ttu-id="d5f4b-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d5f4b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5f4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f4b-117">-DefaultProfile</span></span>
<span data-ttu-id="d5f4b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f4b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d5f4b-119">-DeviceObject</span></span>
<span data-ttu-id="d5f4b-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="d5f4b-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f4b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d5f4b-121">-Name</span></span>
<span data-ttu-id="d5f4b-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="d5f4b-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f4b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5f4b-123">-PassThru</span></span>
<span data-ttu-id="d5f4b-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="d5f4b-124">returns true if successful</span></span>

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

### <span data-ttu-id="d5f4b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f4b-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5f4b-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d5f4b-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f4b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5f4b-127">-ResourceId</span></span>
<span data-ttu-id="d5f4b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5f4b-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="d5f4b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5f4b-129">-Confirm</span></span>
<span data-ttu-id="d5f4b-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5f4b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5f4b-131">-WhatIf</span></span>
<span data-ttu-id="d5f4b-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5f4b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5f4b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f4b-134">CommonParameters</span></span>
<span data-ttu-id="d5f4b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f4b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5f4b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f4b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5f4b-137">INPUTS</span></span>

### <span data-ttu-id="d5f4b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d5f4b-138">System.String</span></span>

### <span data-ttu-id="d5f4b-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d5f4b-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="d5f4b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5f4b-140">OUTPUTS</span></span>

### <span data-ttu-id="d5f4b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5f4b-141">System.Boolean</span></span>

## <span data-ttu-id="d5f4b-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5f4b-142">NOTES</span></span>

## <span data-ttu-id="d5f4b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5f4b-143">RELATED LINKS</span></span>
