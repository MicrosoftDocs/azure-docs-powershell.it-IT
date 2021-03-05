---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: 3463a07219375db06495bd5d50a2fe3b5916e173
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009678"
---
# <span data-ttu-id="99e3c-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="99e3c-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="99e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="99e3c-103">Aggiorna la tabella DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="99e3c-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="99e3c-104">Esegue un'operazione di patch sul lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="99e3c-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="99e3c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99e3c-105">SYNTAX</span></span>

### <span data-ttu-id="99e3c-106">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99e3c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99e3c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e3c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99e3c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99e3c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99e3c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99e3c-109">DESCRIPTION</span></span>
<span data-ttu-id="99e3c-110">Aggiorna la tabella DatabaseDb.</span><span class="sxs-lookup"><span data-stu-id="99e3c-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="99e3c-111">Esegue un'operazione di patch sul lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="99e3c-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="99e3c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99e3c-112">EXAMPLES</span></span>

### <span data-ttu-id="99e3c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99e3c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="99e3c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e3c-114">PARAMETERS</span></span>

### <span data-ttu-id="99e3c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="99e3c-115">-AccountName</span></span>
<span data-ttu-id="99e3c-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="99e3c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99e3c-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="99e3c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="99e3c-118">Valore massimo di velocità effettiva se è abilitata la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="99e3c-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e3c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99e3c-119">-Confirm</span></span>
<span data-ttu-id="99e3c-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e3c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e3c-121">-DefaultProfile</span></span>
<span data-ttu-id="99e3c-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99e3c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e3c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99e3c-123">-InputObject</span></span>
<span data-ttu-id="99e3c-124">Oggetto Table.</span><span class="sxs-lookup"><span data-stu-id="99e3c-124">Table Object.</span></span>

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

### <span data-ttu-id="99e3c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="99e3c-125">-Name</span></span>
<span data-ttu-id="99e3c-126">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="99e3c-126">Name of the Table.</span></span>

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

### <span data-ttu-id="99e3c-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="99e3c-127">-ParentObject</span></span>
<span data-ttu-id="99e3c-128">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="99e3c-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="99e3c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e3c-129">-ResourceGroupName</span></span>
<span data-ttu-id="99e3c-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99e3c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="99e3c-131">-Velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="99e3c-131">-Throughput</span></span>
<span data-ttu-id="99e3c-132">Velocità effettiva della tabella (RU).</span><span class="sxs-lookup"><span data-stu-id="99e3c-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="99e3c-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="99e3c-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e3c-134">-WhatIf</span></span>
<span data-ttu-id="99e3c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99e3c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e3c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99e3c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e3c-137">CommonParameters</span></span>
<span data-ttu-id="99e3c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e3c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99e3c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e3c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="99e3c-140">INPUTS</span></span>

### <span data-ttu-id="99e3c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="99e3c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="99e3c-142">Microsoft.Azure.Commands.EnterpriseDb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="99e3c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="99e3c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99e3c-143">OUTPUTS</span></span>

### <span data-ttu-id="99e3c-144">Microsoft.Azure.Commands.EnterpriseDb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="99e3c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="99e3c-145">Microsoft.Azure.Commands.ExceptionsDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="99e3c-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="99e3c-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="99e3c-146">NOTES</span></span>

## <span data-ttu-id="99e3c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99e3c-147">RELATED LINKS</span></span>
