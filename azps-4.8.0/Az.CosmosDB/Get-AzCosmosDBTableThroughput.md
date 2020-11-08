---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190354"
---
# <span data-ttu-id="0b48a-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="0b48a-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="0b48a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b48a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b48a-103">Ottiene la velocità effettiva di una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0b48a-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="0b48a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b48a-104">SYNTAX</span></span>

### <span data-ttu-id="0b48a-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b48a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b48a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b48a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b48a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b48a-107">DESCRIPTION</span></span>
<span data-ttu-id="0b48a-108">Il cmdlet **Get-AzCosmosDBTableThroughput** ottiene la velocità effettiva di una tabella CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0b48a-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="0b48a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b48a-109">EXAMPLES</span></span>

### <span data-ttu-id="0b48a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b48a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0b48a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b48a-111">PARAMETERS</span></span>

### <span data-ttu-id="0b48a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b48a-112">-AccountName</span></span>
<span data-ttu-id="0b48a-113">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0b48a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0b48a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b48a-114">-DefaultProfile</span></span>
<span data-ttu-id="0b48a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b48a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b48a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b48a-116">-InputObject</span></span>
<span data-ttu-id="0b48a-117">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0b48a-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b48a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b48a-118">-Name</span></span>
<span data-ttu-id="0b48a-119">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0b48a-119">Name of the Table.</span></span>

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

### <span data-ttu-id="0b48a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b48a-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b48a-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b48a-121">Name of resource group.</span></span>

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

### <span data-ttu-id="0b48a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b48a-122">CommonParameters</span></span>
<span data-ttu-id="0b48a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b48a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b48a-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b48a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b48a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b48a-125">INPUTS</span></span>

### <span data-ttu-id="0b48a-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b48a-126">None</span></span>

## <span data-ttu-id="0b48a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b48a-127">OUTPUTS</span></span>

### <span data-ttu-id="0b48a-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0b48a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0b48a-129">Note</span><span class="sxs-lookup"><span data-stu-id="0b48a-129">NOTES</span></span>

## <span data-ttu-id="0b48a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b48a-130">RELATED LINKS</span></span>