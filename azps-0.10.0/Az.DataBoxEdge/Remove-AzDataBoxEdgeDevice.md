---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1878a1ccbdc60ebe4df52dbb762de2436d10086b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863202"
---
# <span data-ttu-id="1dd86-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1dd86-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1dd86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dd86-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd86-103">Rimuove un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="1dd86-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="1dd86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dd86-104">SYNTAX</span></span>

### <span data-ttu-id="1dd86-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dd86-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd86-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd86-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd86-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd86-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd86-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dd86-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd86-109">Il cmdlet **Remove-AzDataBoxEdgeDevice** rimuove la configurazione per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="1dd86-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="1dd86-110">Tieni presente che il dispositivo può essere eliminato solo dopo aver effettuato l'ordine e prima che il dispositivo venga preparato da Microsoft per la spedizione.</span><span class="sxs-lookup"><span data-stu-id="1dd86-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="1dd86-111">Fare riferimento alla documentazione relativa all'eliminazione della risorsa prima di usare questo [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="1dd86-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="1dd86-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dd86-112">EXAMPLES</span></span>

### <span data-ttu-id="1dd86-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dd86-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="1dd86-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dd86-114">PARAMETERS</span></span>

### <span data-ttu-id="1dd86-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dd86-115">-AsJob</span></span>
<span data-ttu-id="1dd86-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1dd86-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dd86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd86-117">-DefaultProfile</span></span>
<span data-ttu-id="1dd86-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd86-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dd86-119">-InputObject</span></span>
<span data-ttu-id="1dd86-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="1dd86-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd86-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dd86-121">-Name</span></span>
<span data-ttu-id="1dd86-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="1dd86-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd86-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dd86-123">-PassThru</span></span>
<span data-ttu-id="1dd86-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1dd86-124">returns true if successful</span></span>

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

### <span data-ttu-id="1dd86-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd86-125">-ResourceGroupName</span></span>
<span data-ttu-id="1dd86-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1dd86-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd86-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd86-127">-ResourceId</span></span>
<span data-ttu-id="1dd86-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd86-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1dd86-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dd86-129">-Confirm</span></span>
<span data-ttu-id="1dd86-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dd86-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd86-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd86-131">-WhatIf</span></span>
<span data-ttu-id="1dd86-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd86-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dd86-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd86-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd86-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd86-134">CommonParameters</span></span>
<span data-ttu-id="1dd86-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd86-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd86-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dd86-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd86-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dd86-137">INPUTS</span></span>

### <span data-ttu-id="1dd86-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd86-138">System.String</span></span>

### <span data-ttu-id="1dd86-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1dd86-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1dd86-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dd86-140">OUTPUTS</span></span>

### <span data-ttu-id="1dd86-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dd86-141">System.Boolean</span></span>

## <span data-ttu-id="1dd86-142">Note</span><span class="sxs-lookup"><span data-stu-id="1dd86-142">NOTES</span></span>

## <span data-ttu-id="1dd86-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dd86-143">RELATED LINKS</span></span>
