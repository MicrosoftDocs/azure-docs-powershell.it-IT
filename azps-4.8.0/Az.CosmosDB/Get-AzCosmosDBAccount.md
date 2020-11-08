---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190837"
---
# <span data-ttu-id="b8178-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="b8178-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="b8178-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8178-102">SYNOPSIS</span></span>
<span data-ttu-id="b8178-103">Ottenere l'account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b8178-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="b8178-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8178-104">SYNTAX</span></span>

### <span data-ttu-id="b8178-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b8178-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8178-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8178-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8178-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8178-107">DESCRIPTION</span></span>
<span data-ttu-id="b8178-108">Il cmdlet **Get-AzCosmosDBAccount** Ottiene l'elenco di tutti gli account di CosmosDB esistenti per un ResourceGroupName specifico e ottiene un singolo account CosmosDB per una determinata ResourceGroupName e AccountName.</span><span class="sxs-lookup"><span data-stu-id="b8178-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="b8178-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8178-109">EXAMPLES</span></span>

### <span data-ttu-id="b8178-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b8178-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="b8178-111">Ottenere l'account di database di CosmosDB con il nome databaseAccountName in ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="b8178-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="b8178-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8178-112">PARAMETERS</span></span>

### <span data-ttu-id="b8178-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8178-113">-DefaultProfile</span></span>
<span data-ttu-id="b8178-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8178-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8178-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8178-115">-Name</span></span>
<span data-ttu-id="b8178-116">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b8178-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8178-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8178-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8178-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b8178-118">Name of resource group.</span></span>

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

### <span data-ttu-id="b8178-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8178-119">-ResourceId</span></span>
<span data-ttu-id="b8178-120">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b8178-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8178-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8178-121">CommonParameters</span></span>
<span data-ttu-id="b8178-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8178-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8178-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8178-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8178-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8178-124">INPUTS</span></span>

### <span data-ttu-id="b8178-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b8178-125">None</span></span>

## <span data-ttu-id="b8178-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8178-126">OUTPUTS</span></span>

### <span data-ttu-id="b8178-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b8178-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b8178-128">Note</span><span class="sxs-lookup"><span data-stu-id="b8178-128">NOTES</span></span>

## <span data-ttu-id="b8178-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8178-129">RELATED LINKS</span></span>
