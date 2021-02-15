---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190951"
---
# <span data-ttu-id="1bf7e-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bf7e-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1bf7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf7e-103">Richiama azioni specifiche su un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1bf7e-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="1bf7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf7e-104">SYNTAX</span></span>

### <span data-ttu-id="1bf7e-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1bf7e-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf7e-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bf7e-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf7e-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bf7e-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf7e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1bf7e-108">DESCRIPTION</span></span>
<span data-ttu-id="1bf7e-109">Il cmdlet **Invoke-AzStackEdgeStorageContainer** richiama le azioni per aggiornare i dati in un contenitore di archiviazione in un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="1bf7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf7e-110">EXAMPLES</span></span>

### <span data-ttu-id="1bf7e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1bf7e-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="1bf7e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1bf7e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="1bf7e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf7e-113">PARAMETERS</span></span>

### <span data-ttu-id="1bf7e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bf7e-114">-AsJob</span></span>
<span data-ttu-id="1bf7e-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1bf7e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bf7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf7e-116">-DefaultProfile</span></span>
<span data-ttu-id="1bf7e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf7e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1bf7e-118">-DeviceName</span></span>
<span data-ttu-id="1bf7e-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="1bf7e-119">Device Name</span></span>

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

### <span data-ttu-id="1bf7e-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1bf7e-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="1bf7e-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="1bf7e-121">Resource Name</span></span>

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

### <span data-ttu-id="1bf7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bf7e-122">-InputObject</span></span>
<span data-ttu-id="1bf7e-123">Fornire un oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="1bf7e-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf7e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf7e-124">-Name</span></span>
<span data-ttu-id="1bf7e-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="1bf7e-125">Resource Name</span></span>

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

### <span data-ttu-id="1bf7e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bf7e-126">-PassThru</span></span>
<span data-ttu-id="1bf7e-127">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="1bf7e-127">returns true if successful</span></span>

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

### <span data-ttu-id="1bf7e-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="1bf7e-128">-RefreshData</span></span>
<span data-ttu-id="1bf7e-129">Aggiornare i metadati contenitore con i dati dal cloud</span><span class="sxs-lookup"><span data-stu-id="1bf7e-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="1bf7e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf7e-130">-ResourceGroupName</span></span>
<span data-ttu-id="1bf7e-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1bf7e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="1bf7e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf7e-132">-ResourceId</span></span>
<span data-ttu-id="1bf7e-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf7e-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="1bf7e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bf7e-134">-Confirm</span></span>
<span data-ttu-id="1bf7e-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf7e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf7e-136">-WhatIf</span></span>
<span data-ttu-id="1bf7e-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bf7e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf7e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf7e-139">CommonParameters</span></span>
<span data-ttu-id="1bf7e-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf7e-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1bf7e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf7e-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="1bf7e-142">INPUTS</span></span>

### <span data-ttu-id="1bf7e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf7e-143">System.String</span></span>

### <span data-ttu-id="1bf7e-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bf7e-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1bf7e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf7e-145">OUTPUTS</span></span>

### <span data-ttu-id="1bf7e-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bf7e-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1bf7e-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="1bf7e-147">NOTES</span></span>

## <span data-ttu-id="1bf7e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf7e-148">RELATED LINKS</span></span>
