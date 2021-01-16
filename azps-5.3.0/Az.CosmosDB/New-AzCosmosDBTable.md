---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487868"
---
# <span data-ttu-id="79bec-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="79bec-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="79bec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79bec-102">SYNOPSIS</span></span>
<span data-ttu-id="79bec-103">Crea una nuova tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="79bec-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="79bec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79bec-104">SYNTAX</span></span>

### <span data-ttu-id="79bec-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79bec-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79bec-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79bec-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79bec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79bec-107">DESCRIPTION</span></span>
<span data-ttu-id="79bec-108">Crea una nuova tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="79bec-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="79bec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79bec-109">EXAMPLES</span></span>

### <span data-ttu-id="79bec-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79bec-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="79bec-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79bec-111">PARAMETERS</span></span>

### <span data-ttu-id="79bec-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79bec-112">-AccountName</span></span>
<span data-ttu-id="79bec-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="79bec-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79bec-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="79bec-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="79bec-115">Valore massimo della velocità effettiva se autoscale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="79bec-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="79bec-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79bec-116">-Confirm</span></span>
<span data-ttu-id="79bec-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79bec-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79bec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bec-118">-DefaultProfile</span></span>
<span data-ttu-id="79bec-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79bec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79bec-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="79bec-120">-Name</span></span>
<span data-ttu-id="79bec-121">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="79bec-121">Name of the Table.</span></span>

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

### <span data-ttu-id="79bec-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79bec-122">-ParentObject</span></span>
<span data-ttu-id="79bec-123">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="79bec-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="79bec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79bec-124">-ResourceGroupName</span></span>
<span data-ttu-id="79bec-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79bec-125">Name of resource group.</span></span>

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

### <span data-ttu-id="79bec-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="79bec-126">-Throughput</span></span>
<span data-ttu-id="79bec-127">La velocità effettiva della tabella (RU/s).</span><span class="sxs-lookup"><span data-stu-id="79bec-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="79bec-128">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="79bec-128">Default value is 400.</span></span>

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

### <span data-ttu-id="79bec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79bec-129">-WhatIf</span></span>
<span data-ttu-id="79bec-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79bec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79bec-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79bec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79bec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bec-132">CommonParameters</span></span>
<span data-ttu-id="79bec-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bec-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79bec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bec-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79bec-135">INPUTS</span></span>

### <span data-ttu-id="79bec-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="79bec-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="79bec-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79bec-137">OUTPUTS</span></span>

### <span data-ttu-id="79bec-138">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="79bec-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="79bec-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="79bec-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="79bec-140">Note</span><span class="sxs-lookup"><span data-stu-id="79bec-140">NOTES</span></span>

## <span data-ttu-id="79bec-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79bec-141">RELATED LINKS</span></span>
