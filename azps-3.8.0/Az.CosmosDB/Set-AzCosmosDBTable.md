---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020151"
---
# <span data-ttu-id="1d17b-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="1d17b-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="1d17b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d17b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d17b-103">Imposta la tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1d17b-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="1d17b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d17b-104">SYNTAX</span></span>

### <span data-ttu-id="1d17b-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d17b-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d17b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d17b-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d17b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d17b-107">DESCRIPTION</span></span>
<span data-ttu-id="1d17b-108">Il cmdlet **set-AzCosmosDBTable** crea una nuova tabella o aggiorna una tabella esistente, sostituendo completamente la tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="1d17b-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="1d17b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d17b-109">EXAMPLES</span></span>

### <span data-ttu-id="1d17b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d17b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="1d17b-111">L'oggetto Resource contiene le proprietà _rid, _ts, _ ETag della tabella.</span><span class="sxs-lookup"><span data-stu-id="1d17b-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="1d17b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d17b-112">PARAMETERS</span></span>

### <span data-ttu-id="1d17b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d17b-113">-AccountName</span></span>
<span data-ttu-id="1d17b-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1d17b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d17b-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d17b-115">-Confirm</span></span>
<span data-ttu-id="1d17b-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d17b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d17b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d17b-117">-DefaultProfile</span></span>
<span data-ttu-id="1d17b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d17b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d17b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d17b-119">-InputObject</span></span>
<span data-ttu-id="1d17b-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1d17b-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d17b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d17b-121">-Name</span></span>
<span data-ttu-id="1d17b-122">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="1d17b-122">Name of the Table.</span></span>

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

### <span data-ttu-id="1d17b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d17b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d17b-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d17b-124">Name of resource group.</span></span>

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

### <span data-ttu-id="1d17b-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1d17b-125">-Throughput</span></span>
<span data-ttu-id="1d17b-126">La velocità effettiva della tabella (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1d17b-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="1d17b-127">Il valore predefinito è 400.</span><span class="sxs-lookup"><span data-stu-id="1d17b-127">Default value is 400.</span></span>

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

### <span data-ttu-id="1d17b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d17b-128">-WhatIf</span></span>
<span data-ttu-id="1d17b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d17b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d17b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d17b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d17b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d17b-131">CommonParameters</span></span>
<span data-ttu-id="1d17b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d17b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d17b-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d17b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d17b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d17b-134">INPUTS</span></span>

### <span data-ttu-id="1d17b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1d17b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1d17b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d17b-136">OUTPUTS</span></span>

### <span data-ttu-id="1d17b-137">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1d17b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="1d17b-138">Note</span><span class="sxs-lookup"><span data-stu-id="1d17b-138">NOTES</span></span>

## <span data-ttu-id="1d17b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d17b-139">RELATED LINKS</span></span>
