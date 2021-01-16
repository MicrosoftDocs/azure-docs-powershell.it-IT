---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352276"
---
# <span data-ttu-id="39ec5-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="39ec5-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="39ec5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="39ec5-103">Rimuove un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="39ec5-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="39ec5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39ec5-104">SYNTAX</span></span>

### <span data-ttu-id="39ec5-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39ec5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ec5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39ec5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ec5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39ec5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ec5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39ec5-108">DESCRIPTION</span></span>
<span data-ttu-id="39ec5-109">Il cmdlet **Remove-AzStackEdgeDevice** consente di rimuovere la configurazione per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="39ec5-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="39ec5-110">Tieni presente che il dispositivo può essere eliminato solo dopo aver effettuato l'ordine e prima che il dispositivo venga preparato da Microsoft per la spedizione.</span><span class="sxs-lookup"><span data-stu-id="39ec5-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="39ec5-111">Fare riferimento alla documentazione relativa all'eliminazione della risorsa prima di usare questo [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="39ec5-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="39ec5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39ec5-112">EXAMPLES</span></span>

### <span data-ttu-id="39ec5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39ec5-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="39ec5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39ec5-114">PARAMETERS</span></span>

### <span data-ttu-id="39ec5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39ec5-115">-AsJob</span></span>
<span data-ttu-id="39ec5-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="39ec5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39ec5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ec5-117">-DefaultProfile</span></span>
<span data-ttu-id="39ec5-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39ec5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39ec5-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="39ec5-119">-DeviceObject</span></span>
<span data-ttu-id="39ec5-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="39ec5-120">Input Object</span></span>

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

### <span data-ttu-id="39ec5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="39ec5-121">-Name</span></span>
<span data-ttu-id="39ec5-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="39ec5-122">Resource Name</span></span>

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

### <span data-ttu-id="39ec5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39ec5-123">-PassThru</span></span>
<span data-ttu-id="39ec5-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="39ec5-124">returns true if successful</span></span>

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

### <span data-ttu-id="39ec5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ec5-125">-ResourceGroupName</span></span>
<span data-ttu-id="39ec5-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="39ec5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="39ec5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39ec5-127">-ResourceId</span></span>
<span data-ttu-id="39ec5-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="39ec5-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="39ec5-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39ec5-129">-Confirm</span></span>
<span data-ttu-id="39ec5-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39ec5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ec5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ec5-131">-WhatIf</span></span>
<span data-ttu-id="39ec5-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39ec5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39ec5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39ec5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ec5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ec5-134">CommonParameters</span></span>
<span data-ttu-id="39ec5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39ec5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ec5-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39ec5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ec5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39ec5-137">INPUTS</span></span>

### <span data-ttu-id="39ec5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="39ec5-138">System.String</span></span>

### <span data-ttu-id="39ec5-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="39ec5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="39ec5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39ec5-140">OUTPUTS</span></span>

### <span data-ttu-id="39ec5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39ec5-141">System.Boolean</span></span>

## <span data-ttu-id="39ec5-142">Note</span><span class="sxs-lookup"><span data-stu-id="39ec5-142">NOTES</span></span>

## <span data-ttu-id="39ec5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39ec5-143">RELATED LINKS</span></span>
