---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022840"
---
# <span data-ttu-id="58e1d-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="58e1d-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="58e1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="58e1d-103">Ottiene una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="58e1d-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="58e1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e1d-104">SYNTAX</span></span>

### <span data-ttu-id="58e1d-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58e1d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58e1d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e1d-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e1d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e1d-107">DESCRIPTION</span></span>
<span data-ttu-id="58e1d-108">Il cmdlet **Get-AzCosmosDBTable** ottiene una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="58e1d-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="58e1d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e1d-109">EXAMPLES</span></span>

### <span data-ttu-id="58e1d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58e1d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="58e1d-111">L'oggetto Resource contiene le proprietà _rid, _ts, _ ETag della tabella.</span><span class="sxs-lookup"><span data-stu-id="58e1d-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="58e1d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58e1d-112">PARAMETERS</span></span>

### <span data-ttu-id="58e1d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58e1d-113">-AccountName</span></span>
<span data-ttu-id="58e1d-114">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="58e1d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="58e1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e1d-115">-DefaultProfile</span></span>
<span data-ttu-id="58e1d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58e1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e1d-117">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="58e1d-117">-Detailed</span></span>
<span data-ttu-id="58e1d-118">Se specificato, il cmdlet restituisce la tabella con il valore della velocità effettiva corrispondente.</span><span class="sxs-lookup"><span data-stu-id="58e1d-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e1d-119">-InputObject</span></span>
<span data-ttu-id="58e1d-120">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="58e1d-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e1d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="58e1d-121">-Name</span></span>
<span data-ttu-id="58e1d-122">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="58e1d-122">Name of the Table.</span></span>

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

### <span data-ttu-id="58e1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="58e1d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58e1d-124">Name of resource group.</span></span>

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

### <span data-ttu-id="58e1d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e1d-125">CommonParameters</span></span>
<span data-ttu-id="58e1d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e1d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e1d-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58e1d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e1d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58e1d-128">INPUTS</span></span>

### <span data-ttu-id="58e1d-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58e1d-129">None</span></span>

## <span data-ttu-id="58e1d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e1d-130">OUTPUTS</span></span>

### <span data-ttu-id="58e1d-131">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="58e1d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="58e1d-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="58e1d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="58e1d-133">Note</span><span class="sxs-lookup"><span data-stu-id="58e1d-133">NOTES</span></span>

## <span data-ttu-id="58e1d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e1d-134">RELATED LINKS</span></span>
