---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020903"
---
# <span data-ttu-id="8fd11-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="8fd11-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="8fd11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fd11-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd11-103">Rimuove un pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8fd11-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8fd11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fd11-104">SYNTAX</span></span>

### <span data-ttu-id="8fd11-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8fd11-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd11-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd11-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd11-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd11-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fd11-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fd11-108">DESCRIPTION</span></span>
<span data-ttu-id="8fd11-109">Il cmdlet **Remove-AzSqlInstancePool** rimuove un pool di istanze SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd11-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8fd11-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fd11-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd11-111">Esempio 1: rimuovere un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="8fd11-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="8fd11-112">Esempio 2: rimuovere un pool di istanze in base all'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="8fd11-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="8fd11-113">Esempio 3: rimuovere un pool di istanze da un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="8fd11-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="8fd11-114">Questo comando rimuove un pool di istanze denominato instancePool0.</span><span class="sxs-lookup"><span data-stu-id="8fd11-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="8fd11-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fd11-115">PARAMETERS</span></span>

### <span data-ttu-id="8fd11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd11-116">-DefaultProfile</span></span>
<span data-ttu-id="8fd11-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fd11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fd11-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fd11-118">-InputObject</span></span>
<span data-ttu-id="8fd11-119">Oggetto pool di istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8fd11-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="8fd11-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fd11-120">-Name</span></span>
<span data-ttu-id="8fd11-121">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="8fd11-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="8fd11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd11-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fd11-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8fd11-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8fd11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fd11-124">-ResourceId</span></span>
<span data-ttu-id="8fd11-125">ID risorsa del pool di istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8fd11-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="8fd11-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8fd11-126">-Confirm</span></span>
<span data-ttu-id="8fd11-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd11-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd11-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd11-128">-WhatIf</span></span>
<span data-ttu-id="8fd11-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fd11-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd11-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fd11-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd11-131">CommonParameters</span></span>
<span data-ttu-id="8fd11-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd11-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fd11-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd11-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fd11-134">INPUTS</span></span>

### <span data-ttu-id="8fd11-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="8fd11-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="8fd11-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd11-136">System.String</span></span>

## <span data-ttu-id="8fd11-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fd11-137">OUTPUTS</span></span>

### <span data-ttu-id="8fd11-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="8fd11-138">System.Object</span></span>
## <span data-ttu-id="8fd11-139">Note</span><span class="sxs-lookup"><span data-stu-id="8fd11-139">NOTES</span></span>

## <span data-ttu-id="8fd11-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fd11-140">RELATED LINKS</span></span>
