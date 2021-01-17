---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372886"
---
# <span data-ttu-id="b4a24-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="b4a24-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="b4a24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4a24-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a24-103">Aggiorna la tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b4a24-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="b4a24-104">Esegue un'operazione di patch lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="b4a24-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="b4a24-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4a24-105">SYNTAX</span></span>

### <span data-ttu-id="b4a24-106">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4a24-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a24-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4a24-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a24-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4a24-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4a24-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4a24-109">DESCRIPTION</span></span>
<span data-ttu-id="b4a24-110">Aggiorna la tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b4a24-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="b4a24-111">Esegue un'operazione di patch lato client leggendo la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="b4a24-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="b4a24-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4a24-112">EXAMPLES</span></span>

### <span data-ttu-id="b4a24-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4a24-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="b4a24-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4a24-114">PARAMETERS</span></span>

### <span data-ttu-id="b4a24-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4a24-115">-AccountName</span></span>
<span data-ttu-id="b4a24-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b4a24-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b4a24-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b4a24-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b4a24-118">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b4a24-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b4a24-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4a24-119">-Confirm</span></span>
<span data-ttu-id="b4a24-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a24-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a24-121">-DefaultProfile</span></span>
<span data-ttu-id="b4a24-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a24-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a24-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a24-123">-InputObject</span></span>
<span data-ttu-id="b4a24-124">Oggetto Table.</span><span class="sxs-lookup"><span data-stu-id="b4a24-124">Table Object.</span></span>

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

### <span data-ttu-id="b4a24-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4a24-125">-Name</span></span>
<span data-ttu-id="b4a24-126">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="b4a24-126">Name of the Table.</span></span>

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

### <span data-ttu-id="b4a24-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4a24-127">-ParentObject</span></span>
<span data-ttu-id="b4a24-128">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b4a24-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b4a24-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a24-129">-ResourceGroupName</span></span>
<span data-ttu-id="b4a24-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4a24-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b4a24-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="b4a24-131">-Throughput</span></span>
<span data-ttu-id="b4a24-132">La velocità effettiva della tabella (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b4a24-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="b4a24-133">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="b4a24-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b4a24-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a24-134">-WhatIf</span></span>
<span data-ttu-id="b4a24-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4a24-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a24-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4a24-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a24-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a24-137">CommonParameters</span></span>
<span data-ttu-id="b4a24-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a24-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a24-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4a24-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a24-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4a24-140">INPUTS</span></span>

### <span data-ttu-id="b4a24-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b4a24-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b4a24-142">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b4a24-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="b4a24-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4a24-143">OUTPUTS</span></span>

### <span data-ttu-id="b4a24-144">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b4a24-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="b4a24-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b4a24-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b4a24-146">Note</span><span class="sxs-lookup"><span data-stu-id="b4a24-146">NOTES</span></span>

## <span data-ttu-id="b4a24-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4a24-147">RELATED LINKS</span></span>
