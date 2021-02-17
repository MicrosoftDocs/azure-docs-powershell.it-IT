---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186303"
---
# <span data-ttu-id="6c017-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c017-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6c017-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c017-102">SYNOPSIS</span></span>
<span data-ttu-id="6c017-103">Rimuove un contenitore di archiviazione per l'account Di archiviazione Edge in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c017-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="6c017-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c017-104">SYNTAX</span></span>

### <span data-ttu-id="6c017-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c017-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c017-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c017-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c017-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c017-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c017-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c017-108">DESCRIPTION</span></span>
<span data-ttu-id="6c017-109">Il cmdlet **Remove-AzDataBoxEdgeStorageContainer rimuove** un contenitore di archiviazione associato per l'account Di archiviazione Edge in un dispositivo Edge della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="6c017-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="6c017-110">È possibile specificare il nome del contenitore di archiviazione da rimuovere come parametro.</span><span class="sxs-lookup"><span data-stu-id="6c017-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="6c017-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c017-111">EXAMPLES</span></span>

### <span data-ttu-id="6c017-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c017-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="6c017-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c017-113">PARAMETERS</span></span>

### <span data-ttu-id="6c017-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c017-114">-AsJob</span></span>
<span data-ttu-id="6c017-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6c017-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c017-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c017-116">-DefaultProfile</span></span>
<span data-ttu-id="6c017-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c017-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c017-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6c017-118">-DeviceName</span></span>
<span data-ttu-id="6c017-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="6c017-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c017-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6c017-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="6c017-121">Fornisci il nome dell'account EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="6c017-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c017-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c017-122">-InputObject</span></span>
<span data-ttu-id="6c017-123">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="6c017-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c017-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6c017-124">-Name</span></span>
<span data-ttu-id="6c017-125">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="6c017-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c017-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c017-126">-PassThru</span></span>
<span data-ttu-id="6c017-127">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="6c017-127">returns true if successful</span></span>

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

### <span data-ttu-id="6c017-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c017-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c017-129">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6c017-129">Resource Group Name</span></span>

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

### <span data-ttu-id="6c017-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c017-130">-ResourceId</span></span>
<span data-ttu-id="6c017-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c017-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="6c017-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c017-132">-Confirm</span></span>
<span data-ttu-id="6c017-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c017-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c017-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c017-134">-WhatIf</span></span>
<span data-ttu-id="6c017-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c017-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c017-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c017-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c017-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c017-137">CommonParameters</span></span>
<span data-ttu-id="6c017-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c017-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c017-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c017-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c017-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c017-140">INPUTS</span></span>

### <span data-ttu-id="6c017-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6c017-141">System.String</span></span>

### <span data-ttu-id="6c017-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c017-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="6c017-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c017-143">OUTPUTS</span></span>

### <span data-ttu-id="6c017-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c017-144">System.Boolean</span></span>

## <span data-ttu-id="6c017-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c017-145">NOTES</span></span>

## <span data-ttu-id="6c017-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c017-146">RELATED LINKS</span></span>
