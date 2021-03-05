---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 0a7874079b7de782fa7471e9087f04fdc3a9e754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967406"
---
# <span data-ttu-id="bdeb8-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="bdeb8-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="bdeb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdeb8-102">SYNOPSIS</span></span>
<span data-ttu-id="bdeb8-103">Rimuove un pool di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bdeb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdeb8-104">SYNTAX</span></span>

### <span data-ttu-id="bdeb8-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdeb8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdeb8-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdeb8-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdeb8-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdeb8-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdeb8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bdeb8-108">DESCRIPTION</span></span>
<span data-ttu-id="bdeb8-109">Il cmdlet **Remove-AzSqlInstancePool** rimuove un pool di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bdeb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdeb8-110">EXAMPLES</span></span>

### <span data-ttu-id="bdeb8-111">Esempio 1: Rimuovere un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="bdeb8-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="bdeb8-112">Esempio 2: Rimuovere un pool di istanze in base al relativo identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="bdeb8-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="bdeb8-113">Esempio 3: Rimuovere un pool di istanze da un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="bdeb8-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="bdeb8-114">Questo comando rimuove un pool di istanze denominato istanzaPool0.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="bdeb8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdeb8-115">PARAMETERS</span></span>

### <span data-ttu-id="bdeb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdeb8-116">-DefaultProfile</span></span>
<span data-ttu-id="bdeb8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdeb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdeb8-118">-InputObject</span></span>
<span data-ttu-id="bdeb8-119">Oggetto pool di istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bdeb8-120">-Name</span></span>
<span data-ttu-id="bdeb8-121">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdeb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdeb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="bdeb8-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdeb8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdeb8-124">-ResourceId</span></span>
<span data-ttu-id="bdeb8-125">ID della risorsa del pool di istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="bdeb8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdeb8-126">-Confirm</span></span>
<span data-ttu-id="bdeb8-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdeb8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdeb8-128">-WhatIf</span></span>
<span data-ttu-id="bdeb8-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdeb8-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdeb8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdeb8-131">CommonParameters</span></span>
<span data-ttu-id="bdeb8-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdeb8-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bdeb8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdeb8-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="bdeb8-134">INPUTS</span></span>

### <span data-ttu-id="bdeb8-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="bdeb8-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="bdeb8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bdeb8-136">System.String</span></span>

## <span data-ttu-id="bdeb8-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdeb8-137">OUTPUTS</span></span>

### <span data-ttu-id="bdeb8-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="bdeb8-138">System.Object</span></span>
## <span data-ttu-id="bdeb8-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="bdeb8-139">NOTES</span></span>

## <span data-ttu-id="bdeb8-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdeb8-140">RELATED LINKS</span></span>
