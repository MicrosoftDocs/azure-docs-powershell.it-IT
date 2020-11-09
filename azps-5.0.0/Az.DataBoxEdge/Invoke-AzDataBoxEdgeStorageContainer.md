---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298795"
---
# <span data-ttu-id="05f0d-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="05f0d-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="05f0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="05f0d-103">Richiama azioni specifiche in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="05f0d-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="05f0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05f0d-104">SYNTAX</span></span>

### <span data-ttu-id="05f0d-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05f0d-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05f0d-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05f0d-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05f0d-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05f0d-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05f0d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05f0d-108">DESCRIPTION</span></span>
<span data-ttu-id="05f0d-109">Il cmdlet **Invoke-AzDataBoxEdgeStorageContainer** richiama le azioni per aggiornare i dati in un contenitore di archiviazione in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="05f0d-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="05f0d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05f0d-110">EXAMPLES</span></span>

### <span data-ttu-id="05f0d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05f0d-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="05f0d-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="05f0d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="05f0d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05f0d-113">PARAMETERS</span></span>

### <span data-ttu-id="05f0d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05f0d-114">-AsJob</span></span>
<span data-ttu-id="05f0d-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="05f0d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05f0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f0d-116">-DefaultProfile</span></span>
<span data-ttu-id="05f0d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05f0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05f0d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="05f0d-118">-DeviceName</span></span>
<span data-ttu-id="05f0d-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="05f0d-119">Device Name</span></span>

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

### <span data-ttu-id="05f0d-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05f0d-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="05f0d-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="05f0d-121">Resource Name</span></span>

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

### <span data-ttu-id="05f0d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05f0d-122">-InputObject</span></span>
<span data-ttu-id="05f0d-123">Fornisci l'oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="05f0d-123">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="05f0d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="05f0d-124">-Name</span></span>
<span data-ttu-id="05f0d-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="05f0d-125">Resource Name</span></span>

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

### <span data-ttu-id="05f0d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05f0d-126">-PassThru</span></span>
<span data-ttu-id="05f0d-127">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="05f0d-127">returns true if successful</span></span>

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

### <span data-ttu-id="05f0d-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="05f0d-128">-RefreshData</span></span>
<span data-ttu-id="05f0d-129">Aggiornare i metadati del contenitore con i dati del cloud</span><span class="sxs-lookup"><span data-stu-id="05f0d-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="05f0d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f0d-130">-ResourceGroupName</span></span>
<span data-ttu-id="05f0d-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="05f0d-131">Resource Group Name</span></span>

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

### <span data-ttu-id="05f0d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f0d-132">-ResourceId</span></span>
<span data-ttu-id="05f0d-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f0d-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="05f0d-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05f0d-134">-Confirm</span></span>
<span data-ttu-id="05f0d-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05f0d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05f0d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05f0d-136">-WhatIf</span></span>
<span data-ttu-id="05f0d-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05f0d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05f0d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05f0d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05f0d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f0d-139">CommonParameters</span></span>
<span data-ttu-id="05f0d-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f0d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f0d-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05f0d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f0d-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05f0d-142">INPUTS</span></span>

### <span data-ttu-id="05f0d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="05f0d-143">System.String</span></span>

### <span data-ttu-id="05f0d-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="05f0d-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="05f0d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05f0d-145">OUTPUTS</span></span>

### <span data-ttu-id="05f0d-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="05f0d-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="05f0d-147">Note</span><span class="sxs-lookup"><span data-stu-id="05f0d-147">NOTES</span></span>

## <span data-ttu-id="05f0d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05f0d-148">RELATED LINKS</span></span>
