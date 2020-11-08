---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188745"
---
# <span data-ttu-id="97a4e-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97a4e-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="97a4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="97a4e-103">Richiama azioni specifiche in un contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="97a4e-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="97a4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97a4e-104">SYNTAX</span></span>

### <span data-ttu-id="97a4e-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97a4e-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a4e-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a4e-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a4e-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a4e-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a4e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97a4e-108">DESCRIPTION</span></span>
<span data-ttu-id="97a4e-109">Il cmdlet **Invoke-AzStackEdgeStorageContainer** richiama le azioni per aggiornare i dati in un contenitore di archiviazione in un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="97a4e-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="97a4e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97a4e-110">EXAMPLES</span></span>

### <span data-ttu-id="97a4e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97a4e-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="97a4e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="97a4e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="97a4e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97a4e-113">PARAMETERS</span></span>

### <span data-ttu-id="97a4e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97a4e-114">-AsJob</span></span>
<span data-ttu-id="97a4e-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="97a4e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97a4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a4e-116">-DefaultProfile</span></span>
<span data-ttu-id="97a4e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97a4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a4e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="97a4e-118">-DeviceName</span></span>
<span data-ttu-id="97a4e-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="97a4e-119">Device Name</span></span>

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

### <span data-ttu-id="97a4e-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="97a4e-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="97a4e-121">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="97a4e-121">Resource Name</span></span>

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

### <span data-ttu-id="97a4e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97a4e-122">-InputObject</span></span>
<span data-ttu-id="97a4e-123">Fornisci l'oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="97a4e-123">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="97a4e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="97a4e-124">-Name</span></span>
<span data-ttu-id="97a4e-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="97a4e-125">Resource Name</span></span>

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

### <span data-ttu-id="97a4e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97a4e-126">-PassThru</span></span>
<span data-ttu-id="97a4e-127">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="97a4e-127">returns true if successful</span></span>

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

### <span data-ttu-id="97a4e-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="97a4e-128">-RefreshData</span></span>
<span data-ttu-id="97a4e-129">Aggiornare i metadati del contenitore con i dati del cloud</span><span class="sxs-lookup"><span data-stu-id="97a4e-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="97a4e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a4e-130">-ResourceGroupName</span></span>
<span data-ttu-id="97a4e-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="97a4e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="97a4e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a4e-132">-ResourceId</span></span>
<span data-ttu-id="97a4e-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a4e-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="97a4e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97a4e-134">-Confirm</span></span>
<span data-ttu-id="97a4e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a4e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a4e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a4e-136">-WhatIf</span></span>
<span data-ttu-id="97a4e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97a4e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97a4e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97a4e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a4e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a4e-139">CommonParameters</span></span>
<span data-ttu-id="97a4e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a4e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a4e-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97a4e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a4e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97a4e-142">INPUTS</span></span>

### <span data-ttu-id="97a4e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="97a4e-143">System.String</span></span>

### <span data-ttu-id="97a4e-144">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97a4e-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="97a4e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97a4e-145">OUTPUTS</span></span>

### <span data-ttu-id="97a4e-146">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97a4e-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="97a4e-147">Note</span><span class="sxs-lookup"><span data-stu-id="97a4e-147">NOTES</span></span>

## <span data-ttu-id="97a4e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97a4e-148">RELATED LINKS</span></span>
