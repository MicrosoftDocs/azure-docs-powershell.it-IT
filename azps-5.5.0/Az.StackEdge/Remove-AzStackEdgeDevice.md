---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209115"
---
# <span data-ttu-id="bb8eb-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bb8eb-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="bb8eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8eb-103">Rimuove un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="bb8eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb8eb-104">SYNTAX</span></span>

### <span data-ttu-id="bb8eb-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb8eb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb8eb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb8eb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb8eb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb8eb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8eb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb8eb-108">DESCRIPTION</span></span>
<span data-ttu-id="bb8eb-109">Il cmdlet **Remove-AzStackEdgeDevice** rimuove la configurazione per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="bb8eb-110">Tieni presente che il dispositivo può essere eliminato solo dopo aver effettuato l'ordine e prima che il dispositivo venga preparato da Microsoft per la spedizione.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="bb8eb-111">Fare riferimento alla documentazione sull'eliminazione della risorsa prima di usare questo [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="bb8eb-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="bb8eb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb8eb-112">EXAMPLES</span></span>

### <span data-ttu-id="bb8eb-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb8eb-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="bb8eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb8eb-114">PARAMETERS</span></span>

### <span data-ttu-id="bb8eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb8eb-115">-AsJob</span></span>
<span data-ttu-id="bb8eb-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bb8eb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb8eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8eb-117">-DefaultProfile</span></span>
<span data-ttu-id="bb8eb-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8eb-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="bb8eb-119">-DeviceObject</span></span>
<span data-ttu-id="bb8eb-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="bb8eb-120">Input Object</span></span>

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

### <span data-ttu-id="bb8eb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bb8eb-121">-Name</span></span>
<span data-ttu-id="bb8eb-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="bb8eb-122">Resource Name</span></span>

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

### <span data-ttu-id="bb8eb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb8eb-123">-PassThru</span></span>
<span data-ttu-id="bb8eb-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="bb8eb-124">returns true if successful</span></span>

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

### <span data-ttu-id="bb8eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb8eb-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bb8eb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="bb8eb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb8eb-127">-ResourceId</span></span>
<span data-ttu-id="bb8eb-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb8eb-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="bb8eb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb8eb-129">-Confirm</span></span>
<span data-ttu-id="bb8eb-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8eb-131">-WhatIf</span></span>
<span data-ttu-id="bb8eb-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb8eb-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8eb-134">CommonParameters</span></span>
<span data-ttu-id="bb8eb-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8eb-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb8eb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8eb-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb8eb-137">INPUTS</span></span>

### <span data-ttu-id="bb8eb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bb8eb-138">System.String</span></span>

### <span data-ttu-id="bb8eb-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bb8eb-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="bb8eb-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb8eb-140">OUTPUTS</span></span>

### <span data-ttu-id="bb8eb-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb8eb-141">System.Boolean</span></span>

## <span data-ttu-id="bb8eb-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb8eb-142">NOTES</span></span>

## <span data-ttu-id="bb8eb-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb8eb-143">RELATED LINKS</span></span>
