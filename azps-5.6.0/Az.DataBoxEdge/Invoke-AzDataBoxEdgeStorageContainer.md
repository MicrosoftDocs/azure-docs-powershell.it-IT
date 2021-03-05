---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f6607f59e2cc29557c41bf07014c3604fdb1bf47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998071"
---
# <span data-ttu-id="7e20f-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7e20f-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7e20f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e20f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e20f-103">Richiama azioni specifiche su un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e20f-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="7e20f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e20f-104">SYNTAX</span></span>

### <span data-ttu-id="7e20f-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e20f-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e20f-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e20f-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e20f-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e20f-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e20f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7e20f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e20f-109">Il cmdlet **Invoke-AzDataBoxEdgeStorageContainer** richiama le azioni per aggiornare i dati in un contenitore di archiviazione in un dispositivo Edge della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="7e20f-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="7e20f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e20f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e20f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e20f-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="7e20f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7e20f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="7e20f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e20f-113">PARAMETERS</span></span>

### <span data-ttu-id="7e20f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e20f-114">-AsJob</span></span>
<span data-ttu-id="7e20f-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7e20f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e20f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e20f-116">-DefaultProfile</span></span>
<span data-ttu-id="7e20f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e20f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e20f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7e20f-118">-DeviceName</span></span>
<span data-ttu-id="7e20f-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="7e20f-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e20f-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e20f-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7e20f-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="7e20f-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e20f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e20f-122">-InputObject</span></span>
<span data-ttu-id="7e20f-123">Fornire un oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="7e20f-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e20f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7e20f-124">-Name</span></span>
<span data-ttu-id="7e20f-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="7e20f-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e20f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e20f-126">-PassThru</span></span>
<span data-ttu-id="7e20f-127">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="7e20f-127">returns true if successful</span></span>

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

### <span data-ttu-id="7e20f-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="7e20f-128">-RefreshData</span></span>
<span data-ttu-id="7e20f-129">Aggiornare i metadati contenitore con i dati dal cloud</span><span class="sxs-lookup"><span data-stu-id="7e20f-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="7e20f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e20f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7e20f-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7e20f-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e20f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e20f-132">-ResourceId</span></span>
<span data-ttu-id="7e20f-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e20f-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e20f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e20f-134">-Confirm</span></span>
<span data-ttu-id="7e20f-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e20f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e20f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e20f-136">-WhatIf</span></span>
<span data-ttu-id="7e20f-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e20f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e20f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e20f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e20f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e20f-139">CommonParameters</span></span>
<span data-ttu-id="7e20f-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e20f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e20f-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e20f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e20f-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="7e20f-142">INPUTS</span></span>

### <span data-ttu-id="7e20f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7e20f-143">System.String</span></span>

### <span data-ttu-id="7e20f-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7e20f-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7e20f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e20f-145">OUTPUTS</span></span>

### <span data-ttu-id="7e20f-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7e20f-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7e20f-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="7e20f-147">NOTES</span></span>

## <span data-ttu-id="7e20f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e20f-148">RELATED LINKS</span></span>
