---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190836"
---
# <span data-ttu-id="2ebeb-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="2ebeb-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="2ebeb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ebeb-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebeb-103">Get Keys {"ConnectionKeys", "PrimaryReadOnly" o "Keys"} per l'account CosmosDB indicato.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="2ebeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ebeb-104">SYNTAX</span></span>

### <span data-ttu-id="2ebeb-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ebeb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ebeb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ebeb-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ebeb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ebeb-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ebeb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ebeb-108">DESCRIPTION</span></span>
<span data-ttu-id="2ebeb-109">Ottenere l'elenco delle chiavi di connessione.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="2ebeb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ebeb-110">EXAMPLES</span></span>

### <span data-ttu-id="2ebeb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ebeb-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="2ebeb-112">Elenca le chiavi per l'account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="2ebeb-113">Il tipo di chiave può essere valore da: connectionStrings, Keys e ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="2ebeb-114">Il valore predefinito è Keys.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-114">Default is Keys.</span></span>

## <span data-ttu-id="2ebeb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ebeb-115">PARAMETERS</span></span>

### <span data-ttu-id="2ebeb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebeb-116">-DefaultProfile</span></span>
<span data-ttu-id="2ebeb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebeb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ebeb-118">-InputObject</span></span>
<span data-ttu-id="2ebeb-119">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2ebeb-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ebeb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ebeb-120">-Name</span></span>
<span data-ttu-id="2ebeb-121">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ebeb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebeb-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ebeb-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-123">Name of resource group.</span></span>

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

### <span data-ttu-id="2ebeb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ebeb-124">-ResourceId</span></span>
<span data-ttu-id="2ebeb-125">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2ebeb-126">-Digitare</span><span class="sxs-lookup"><span data-stu-id="2ebeb-126">-Type</span></span>
<span data-ttu-id="2ebeb-127">Valore da: {connectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="2ebeb-128">Il valore predefinito è Keys.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-128">Default is Keys.</span></span>

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

### <span data-ttu-id="2ebeb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebeb-129">CommonParameters</span></span>
<span data-ttu-id="2ebeb-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebeb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebeb-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ebeb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebeb-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ebeb-132">INPUTS</span></span>

### <span data-ttu-id="2ebeb-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2ebeb-133">None</span></span>

## <span data-ttu-id="2ebeb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ebeb-134">OUTPUTS</span></span>

### <span data-ttu-id="2ebeb-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2ebeb-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="2ebeb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="2ebeb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="2ebeb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="2ebeb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="2ebeb-138">Note</span><span class="sxs-lookup"><span data-stu-id="2ebeb-138">NOTES</span></span>

## <span data-ttu-id="2ebeb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ebeb-139">RELATED LINKS</span></span>
