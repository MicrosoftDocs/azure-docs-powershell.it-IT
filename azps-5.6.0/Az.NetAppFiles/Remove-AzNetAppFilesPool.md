---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: a62e6093ec5cfdf7244ea83b2dccf07ad07308fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968318"
---
# <span data-ttu-id="631ea-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="631ea-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="631ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631ea-102">SYNOPSIS</span></span>
<span data-ttu-id="631ea-103">Elimina un pool di file (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="631ea-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="631ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="631ea-104">SYNTAX</span></span>

### <span data-ttu-id="631ea-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="631ea-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631ea-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="631ea-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631ea-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="631ea-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631ea-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="631ea-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631ea-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="631ea-109">DESCRIPTION</span></span>
<span data-ttu-id="631ea-110">Il cmdlet **Remove-AzNetAppFilesPool** elimina un pool ANF.</span><span class="sxs-lookup"><span data-stu-id="631ea-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="631ea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="631ea-111">EXAMPLES</span></span>

### <span data-ttu-id="631ea-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="631ea-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="631ea-113">Questo comando elimina il pool ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="631ea-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="631ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631ea-114">PARAMETERS</span></span>

### <span data-ttu-id="631ea-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="631ea-115">-AccountName</span></span>
<span data-ttu-id="631ea-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="631ea-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631ea-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="631ea-117">-AccountObject</span></span>
<span data-ttu-id="631ea-118">Oggetto account contenente il pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="631ea-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="631ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631ea-119">-DefaultProfile</span></span>
<span data-ttu-id="631ea-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="631ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="631ea-121">-InputObject</span></span>
<span data-ttu-id="631ea-122">L'oggetto pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="631ea-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="631ea-123">-Name</span><span class="sxs-lookup"><span data-stu-id="631ea-123">-Name</span></span>
<span data-ttu-id="631ea-124">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="631ea-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631ea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="631ea-125">-PassThru</span></span>
<span data-ttu-id="631ea-126">Restituire se il pool specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="631ea-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="631ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="631ea-128">Gruppo di risorse del pool ANF</span><span class="sxs-lookup"><span data-stu-id="631ea-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631ea-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="631ea-129">-ResourceId</span></span>
<span data-ttu-id="631ea-130">ID risorsa del pool ANF</span><span class="sxs-lookup"><span data-stu-id="631ea-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="631ea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="631ea-131">-Confirm</span></span>
<span data-ttu-id="631ea-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="631ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631ea-133">-WhatIf</span></span>
<span data-ttu-id="631ea-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="631ea-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="631ea-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="631ea-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631ea-136">CommonParameters</span></span>
<span data-ttu-id="631ea-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631ea-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="631ea-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631ea-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="631ea-139">INPUTS</span></span>

### <span data-ttu-id="631ea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="631ea-140">System.String</span></span>

### <span data-ttu-id="631ea-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="631ea-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="631ea-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="631ea-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="631ea-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="631ea-143">OUTPUTS</span></span>

### <span data-ttu-id="631ea-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="631ea-144">System.Boolean</span></span>

## <span data-ttu-id="631ea-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="631ea-145">NOTES</span></span>

## <span data-ttu-id="631ea-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="631ea-146">RELATED LINKS</span></span>
