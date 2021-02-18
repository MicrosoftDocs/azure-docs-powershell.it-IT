---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181399"
---
# <span data-ttu-id="9a47e-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9a47e-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9a47e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a47e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a47e-103">Ottenere l'account diDbDb.</span><span class="sxs-lookup"><span data-stu-id="9a47e-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="9a47e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a47e-104">SYNTAX</span></span>

### <span data-ttu-id="9a47e-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a47e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a47e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a47e-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a47e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9a47e-107">DESCRIPTION</span></span>
<span data-ttu-id="9a47e-108">Il cmdlet **Get-AzCosmosDBAccount** ottiene l'elenco di tutti gli account Dibdb esistenti per un determinato ResourceGroupName e un singolo account ClusterDB per un determinato ResourceGroupName e AccountName.</span><span class="sxs-lookup"><span data-stu-id="9a47e-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="9a47e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a47e-109">EXAMPLES</span></span>

### <span data-ttu-id="9a47e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a47e-110">Example 1</span></span>
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

<span data-ttu-id="9a47e-111">Ottenere l'account di databaseDbDb con nome databaseAccountName in ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9a47e-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9a47e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a47e-112">PARAMETERS</span></span>

### <span data-ttu-id="9a47e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a47e-113">-DefaultProfile</span></span>
<span data-ttu-id="9a47e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a47e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a47e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9a47e-115">-Name</span></span>
<span data-ttu-id="9a47e-116">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="9a47e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9a47e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a47e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a47e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a47e-118">Name of resource group.</span></span>

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

### <span data-ttu-id="9a47e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a47e-119">-ResourceId</span></span>
<span data-ttu-id="9a47e-120">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9a47e-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="9a47e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a47e-121">CommonParameters</span></span>
<span data-ttu-id="9a47e-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a47e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a47e-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a47e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a47e-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="9a47e-124">INPUTS</span></span>

### <span data-ttu-id="9a47e-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9a47e-125">None</span></span>

## <span data-ttu-id="9a47e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a47e-126">OUTPUTS</span></span>

### <span data-ttu-id="9a47e-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9a47e-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9a47e-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="9a47e-128">NOTES</span></span>

## <span data-ttu-id="9a47e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a47e-129">RELATED LINKS</span></span>
