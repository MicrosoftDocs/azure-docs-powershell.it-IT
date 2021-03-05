---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 2511ddc7174d4b76ec6d5df5bcbcd334f423a882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996853"
---
# <span data-ttu-id="9fb93-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9fb93-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="9fb93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb93-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb93-103">Consente di eseguire la migrazione della velocità effettiva della scala automatica alla velocità effettiva manuale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="9fb93-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9fb93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fb93-104">SYNTAX</span></span>

### <span data-ttu-id="9fb93-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fb93-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb93-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fb93-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb93-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fb93-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9fb93-108">DESCRIPTION</span></span>
<span data-ttu-id="9fb93-109">ThroughpyteType paramter definisce la velocità effettiva a cui si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="9fb93-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9fb93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fb93-110">EXAMPLES</span></span>

### <span data-ttu-id="9fb93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fb93-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="9fb93-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fb93-112">PARAMETERS</span></span>

### <span data-ttu-id="9fb93-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9fb93-113">-AccountName</span></span>
<span data-ttu-id="9fb93-114">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="9fb93-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fb93-115">-Confirm</span></span>
<span data-ttu-id="9fb93-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fb93-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb93-117">-DefaultProfile</span></span>
<span data-ttu-id="9fb93-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fb93-119">-InputObject</span></span>
<span data-ttu-id="9fb93-120">Oggetto Table.</span><span class="sxs-lookup"><span data-stu-id="9fb93-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9fb93-121">-Name</span></span>
<span data-ttu-id="9fb93-122">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="9fb93-122">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9fb93-123">-ParentObject</span></span>
<span data-ttu-id="9fb93-124">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="9fb93-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb93-125">-ResourceGroupName</span></span>
<span data-ttu-id="9fb93-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fb93-126">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="9fb93-127">-ThroughputType</span></span>
<span data-ttu-id="9fb93-128">Tipo di velocità effettiva di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="9fb93-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="9fb93-129">I valori possibili sono: Scala automatica, Manuale.</span><span class="sxs-lookup"><span data-stu-id="9fb93-129">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb93-130">-WhatIf</span></span>
<span data-ttu-id="9fb93-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fb93-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb93-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fb93-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb93-133">CommonParameters</span></span>
<span data-ttu-id="9fb93-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb93-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9fb93-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb93-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="9fb93-136">INPUTS</span></span>

### <span data-ttu-id="9fb93-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="9fb93-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="9fb93-138">Microsoft.Azure.Commands.EnterpriseDb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="9fb93-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="9fb93-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fb93-139">OUTPUTS</span></span>

### <span data-ttu-id="9fb93-140">Microsoft.Azure.Commands.EnterpriseDb.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9fb93-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9fb93-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="9fb93-141">NOTES</span></span>

## <span data-ttu-id="9fb93-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fb93-142">RELATED LINKS</span></span>
