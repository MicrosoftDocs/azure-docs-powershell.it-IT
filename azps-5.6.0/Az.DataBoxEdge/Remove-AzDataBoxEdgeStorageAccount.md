---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 44a2cd433b8c0167ff472932d318322d9c932971
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952686"
---
# <span data-ttu-id="0f018-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f018-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="0f018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f018-102">SYNOPSIS</span></span>
<span data-ttu-id="0f018-103">Rimuove l'account di Archiviazione Edge per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f018-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="0f018-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f018-104">SYNTAX</span></span>

### <span data-ttu-id="0f018-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f018-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f018-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f018-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f018-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f018-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f018-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f018-108">DESCRIPTION</span></span>
<span data-ttu-id="0f018-109">Il cmdlet **Remove-AzDataBoxEdgeStorageAccount** rimuove un account di archiviazione Edge associato per un dispositivo Edge di Data Box.</span><span class="sxs-lookup"><span data-stu-id="0f018-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="0f018-110">È possibile specificare il nome dell'account di archiviazione di Microsoft Edge da rimuovere come parametro nel cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f018-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="0f018-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f018-111">EXAMPLES</span></span>

### <span data-ttu-id="0f018-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f018-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="0f018-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f018-113">PARAMETERS</span></span>

### <span data-ttu-id="0f018-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f018-114">-AsJob</span></span>
<span data-ttu-id="0f018-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0f018-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f018-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f018-116">-DefaultProfile</span></span>
<span data-ttu-id="0f018-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f018-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f018-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0f018-118">-DeviceName</span></span>
<span data-ttu-id="0f018-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="0f018-119">Device Name</span></span>

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

### <span data-ttu-id="0f018-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f018-120">-InputObject</span></span>
<span data-ttu-id="0f018-121">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="0f018-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f018-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f018-122">-Name</span></span>
<span data-ttu-id="0f018-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="0f018-123">Resource Name</span></span>

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

### <span data-ttu-id="0f018-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f018-124">-PassThru</span></span>
<span data-ttu-id="0f018-125">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="0f018-125">returns true if successful</span></span>

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

### <span data-ttu-id="0f018-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f018-126">-ResourceGroupName</span></span>
<span data-ttu-id="0f018-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0f018-127">Resource Group Name</span></span>

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

### <span data-ttu-id="0f018-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f018-128">-ResourceId</span></span>
<span data-ttu-id="0f018-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f018-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f018-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f018-130">-Confirm</span></span>
<span data-ttu-id="0f018-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f018-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f018-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f018-132">-WhatIf</span></span>
<span data-ttu-id="0f018-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f018-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f018-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f018-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f018-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f018-135">CommonParameters</span></span>
<span data-ttu-id="0f018-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f018-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f018-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f018-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f018-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f018-138">INPUTS</span></span>

### <span data-ttu-id="0f018-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0f018-139">System.String</span></span>

### <span data-ttu-id="0f018-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f018-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="0f018-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f018-141">OUTPUTS</span></span>

### <span data-ttu-id="0f018-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f018-142">System.Boolean</span></span>

## <span data-ttu-id="0f018-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f018-143">NOTES</span></span>

## <span data-ttu-id="0f018-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f018-144">RELATED LINKS</span></span>
