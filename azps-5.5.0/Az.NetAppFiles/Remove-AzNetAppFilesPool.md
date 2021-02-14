---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190015"
---
# <span data-ttu-id="45c83-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="45c83-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="45c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c83-102">SYNOPSIS</span></span>
<span data-ttu-id="45c83-103">Elimina un pool di file (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="45c83-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="45c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45c83-104">SYNTAX</span></span>

### <span data-ttu-id="45c83-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45c83-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c83-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c83-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c83-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c83-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c83-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c83-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c83-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45c83-109">DESCRIPTION</span></span>
<span data-ttu-id="45c83-110">Il cmdlet **Remove-AzNetAppFilesPool** elimina un pool ANF.</span><span class="sxs-lookup"><span data-stu-id="45c83-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="45c83-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45c83-111">EXAMPLES</span></span>

### <span data-ttu-id="45c83-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45c83-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="45c83-113">Questo comando elimina il pool ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="45c83-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="45c83-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45c83-114">PARAMETERS</span></span>

### <span data-ttu-id="45c83-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="45c83-115">-AccountName</span></span>
<span data-ttu-id="45c83-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="45c83-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="45c83-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="45c83-117">-AccountObject</span></span>
<span data-ttu-id="45c83-118">Oggetto account contenente il pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="45c83-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="45c83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c83-119">-DefaultProfile</span></span>
<span data-ttu-id="45c83-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45c83-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45c83-121">-InputObject</span></span>
<span data-ttu-id="45c83-122">L'oggetto pool da rimuovere</span><span class="sxs-lookup"><span data-stu-id="45c83-122">The pool object to remove</span></span>

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

### <span data-ttu-id="45c83-123">-Name</span><span class="sxs-lookup"><span data-stu-id="45c83-123">-Name</span></span>
<span data-ttu-id="45c83-124">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="45c83-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="45c83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45c83-125">-PassThru</span></span>
<span data-ttu-id="45c83-126">Restituire se il pool specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="45c83-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="45c83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c83-127">-ResourceGroupName</span></span>
<span data-ttu-id="45c83-128">Gruppo di risorse del pool ANF</span><span class="sxs-lookup"><span data-stu-id="45c83-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="45c83-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c83-129">-ResourceId</span></span>
<span data-ttu-id="45c83-130">ID risorsa del pool ANF</span><span class="sxs-lookup"><span data-stu-id="45c83-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="45c83-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45c83-131">-Confirm</span></span>
<span data-ttu-id="45c83-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c83-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c83-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c83-133">-WhatIf</span></span>
<span data-ttu-id="45c83-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45c83-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c83-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45c83-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c83-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c83-136">CommonParameters</span></span>
<span data-ttu-id="45c83-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c83-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c83-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45c83-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c83-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="45c83-139">INPUTS</span></span>

### <span data-ttu-id="45c83-140">System.String</span><span class="sxs-lookup"><span data-stu-id="45c83-140">System.String</span></span>

### <span data-ttu-id="45c83-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="45c83-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="45c83-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="45c83-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="45c83-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45c83-143">OUTPUTS</span></span>

### <span data-ttu-id="45c83-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45c83-144">System.Boolean</span></span>

## <span data-ttu-id="45c83-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="45c83-145">NOTES</span></span>

## <span data-ttu-id="45c83-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45c83-146">RELATED LINKS</span></span>
