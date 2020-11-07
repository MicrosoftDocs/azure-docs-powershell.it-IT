---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: 6c0fb28010aff759c406ddd04db281dc05ce1f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864507"
---
# <span data-ttu-id="fd74e-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="fd74e-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="fd74e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd74e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd74e-103">Get Keys {"ConnectionKeys", "PrimaryReadOnly" o "Keys"} per l'account CosmosDB indicato.</span><span class="sxs-lookup"><span data-stu-id="fd74e-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="fd74e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd74e-104">SYNTAX</span></span>

### <span data-ttu-id="fd74e-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd74e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd74e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd74e-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd74e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd74e-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd74e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd74e-108">DESCRIPTION</span></span>
<span data-ttu-id="fd74e-109">Ottenere l'elenco delle chiavi di connessione.</span><span class="sxs-lookup"><span data-stu-id="fd74e-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="fd74e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd74e-110">EXAMPLES</span></span>

### <span data-ttu-id="fd74e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd74e-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="fd74e-112">Elenca le chiavi per l'account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="fd74e-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="fd74e-113">Il tipo di chiave può essere valore da: connectionStrings, Keys e ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="fd74e-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="fd74e-114">Il valore predefinito è Keys.</span><span class="sxs-lookup"><span data-stu-id="fd74e-114">Default is Keys.</span></span>

## <span data-ttu-id="fd74e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd74e-115">PARAMETERS</span></span>

### <span data-ttu-id="fd74e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd74e-116">-DefaultProfile</span></span>
<span data-ttu-id="fd74e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd74e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd74e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd74e-118">-InputObject</span></span>
<span data-ttu-id="fd74e-119">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fd74e-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd74e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd74e-120">-Name</span></span>
<span data-ttu-id="fd74e-121">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="fd74e-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fd74e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd74e-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd74e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd74e-123">Name of resource group.</span></span>

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

### <span data-ttu-id="fd74e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd74e-124">-ResourceId</span></span>
<span data-ttu-id="fd74e-125">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd74e-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="fd74e-126">-Digitare</span><span class="sxs-lookup"><span data-stu-id="fd74e-126">-Type</span></span>
<span data-ttu-id="fd74e-127">Valore da: {connectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="fd74e-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="fd74e-128">Il valore predefinito è Keys.</span><span class="sxs-lookup"><span data-stu-id="fd74e-128">Default is Keys.</span></span>

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

### <span data-ttu-id="fd74e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd74e-129">CommonParameters</span></span>
<span data-ttu-id="fd74e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd74e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd74e-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd74e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd74e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd74e-132">INPUTS</span></span>

### <span data-ttu-id="fd74e-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fd74e-133">None</span></span>

## <span data-ttu-id="fd74e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd74e-134">OUTPUTS</span></span>

### <span data-ttu-id="fd74e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fd74e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="fd74e-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="fd74e-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="fd74e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="fd74e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="fd74e-138">Note</span><span class="sxs-lookup"><span data-stu-id="fd74e-138">NOTES</span></span>

## <span data-ttu-id="fd74e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd74e-139">RELATED LINKS</span></span>
