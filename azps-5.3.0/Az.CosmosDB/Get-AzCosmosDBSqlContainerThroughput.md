---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477507"
---
# <span data-ttu-id="b3e07-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="b3e07-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="b3e07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3e07-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e07-103">Ottiene le impostazioni della velocità effettiva corrispondenti a un contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b3e07-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="b3e07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3e07-104">SYNTAX</span></span>

### <span data-ttu-id="b3e07-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3e07-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3e07-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3e07-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e07-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3e07-107">DESCRIPTION</span></span>
<span data-ttu-id="b3e07-108">Il cmdlet **Get-AzCosmosDBSqlContainerThroughput** ottiene le impostazioni della velocità effettiva corrispondenti a un contenitore SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b3e07-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="b3e07-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3e07-109">EXAMPLES</span></span>

### <span data-ttu-id="b3e07-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3e07-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="b3e07-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3e07-111">PARAMETERS</span></span>

### <span data-ttu-id="b3e07-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3e07-112">-AccountName</span></span>
<span data-ttu-id="b3e07-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b3e07-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3e07-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3e07-114">-DatabaseName</span></span>
<span data-ttu-id="b3e07-115">Nome database.</span><span class="sxs-lookup"><span data-stu-id="b3e07-115">Database name.</span></span>

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

### <span data-ttu-id="b3e07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e07-116">-DefaultProfile</span></span>
<span data-ttu-id="b3e07-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e07-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e07-118">-InputObject</span></span>
<span data-ttu-id="b3e07-119">Oggetto contenitore SQL.</span><span class="sxs-lookup"><span data-stu-id="b3e07-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e07-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3e07-120">-Name</span></span>
<span data-ttu-id="b3e07-121">Nome contenitore.</span><span class="sxs-lookup"><span data-stu-id="b3e07-121">Container name.</span></span>

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

### <span data-ttu-id="b3e07-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e07-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3e07-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3e07-123">Name of resource group.</span></span>

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

### <span data-ttu-id="b3e07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e07-124">CommonParameters</span></span>
<span data-ttu-id="b3e07-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e07-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3e07-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e07-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3e07-127">INPUTS</span></span>

### <span data-ttu-id="b3e07-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b3e07-128">None</span></span>

## <span data-ttu-id="b3e07-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3e07-129">OUTPUTS</span></span>

### <span data-ttu-id="b3e07-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b3e07-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b3e07-131">Note</span><span class="sxs-lookup"><span data-stu-id="b3e07-131">NOTES</span></span>

## <span data-ttu-id="b3e07-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3e07-132">RELATED LINKS</span></span>
