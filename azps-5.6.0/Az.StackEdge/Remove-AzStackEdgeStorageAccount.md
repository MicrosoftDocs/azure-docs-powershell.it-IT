---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 0a573f8fa293d2c3e4c84eced54c88eb77032970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005118"
---
# <span data-ttu-id="9572b-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9572b-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="9572b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9572b-102">SYNOPSIS</span></span>
<span data-ttu-id="9572b-103">Rimuove l'account di Archiviazione Edge per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9572b-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="9572b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9572b-104">SYNTAX</span></span>

### <span data-ttu-id="9572b-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9572b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9572b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9572b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9572b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9572b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9572b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9572b-108">DESCRIPTION</span></span>
<span data-ttu-id="9572b-109">Il cmdlet **Remove-AzStackEdgeStorageAccount** rimuove un account di archiviazione Edge associato per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="9572b-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="9572b-110">È possibile specificare il nome dell'account di archiviazione di Microsoft Edge da rimuovere come parametro nel cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9572b-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="9572b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9572b-111">EXAMPLES</span></span>

### <span data-ttu-id="9572b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9572b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="9572b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9572b-113">PARAMETERS</span></span>

### <span data-ttu-id="9572b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9572b-114">-AsJob</span></span>
<span data-ttu-id="9572b-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9572b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9572b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9572b-116">-DefaultProfile</span></span>
<span data-ttu-id="9572b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9572b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9572b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9572b-118">-DeviceName</span></span>
<span data-ttu-id="9572b-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="9572b-119">Device Name</span></span>

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

### <span data-ttu-id="9572b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9572b-120">-InputObject</span></span>
<span data-ttu-id="9572b-121">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="9572b-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9572b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9572b-122">-Name</span></span>
<span data-ttu-id="9572b-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="9572b-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9572b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9572b-124">-PassThru</span></span>
<span data-ttu-id="9572b-125">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="9572b-125">returns true if successful</span></span>

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

### <span data-ttu-id="9572b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9572b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9572b-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9572b-127">Resource Group Name</span></span>

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

### <span data-ttu-id="9572b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9572b-128">-ResourceId</span></span>
<span data-ttu-id="9572b-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9572b-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="9572b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9572b-130">-Confirm</span></span>
<span data-ttu-id="9572b-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9572b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9572b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9572b-132">-WhatIf</span></span>
<span data-ttu-id="9572b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9572b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9572b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9572b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9572b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9572b-135">CommonParameters</span></span>
<span data-ttu-id="9572b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9572b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9572b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9572b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9572b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9572b-138">INPUTS</span></span>

### <span data-ttu-id="9572b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9572b-139">System.String</span></span>

### <span data-ttu-id="9572b-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9572b-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="9572b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9572b-141">OUTPUTS</span></span>

### <span data-ttu-id="9572b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9572b-142">System.Boolean</span></span>

## <span data-ttu-id="9572b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="9572b-143">NOTES</span></span>

## <span data-ttu-id="9572b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9572b-144">RELATED LINKS</span></span>
