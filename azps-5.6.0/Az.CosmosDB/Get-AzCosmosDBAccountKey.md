---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: c143fed64e99dd9f564b4375c4ef20e5b5ad4354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983726"
---
# <span data-ttu-id="44fa3-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="44fa3-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="44fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="44fa3-103">Ottenere keys{"ConnectionKeys", "PrimaryReadOnly" o "Keys"} per l'account Dib3 specificato.</span><span class="sxs-lookup"><span data-stu-id="44fa3-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="44fa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44fa3-104">SYNTAX</span></span>

### <span data-ttu-id="44fa3-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44fa3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fa3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fa3-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44fa3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fa3-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44fa3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="44fa3-109">Ottenere l'elenco delle chiavi di connessione.</span><span class="sxs-lookup"><span data-stu-id="44fa3-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="44fa3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44fa3-110">EXAMPLES</span></span>

### <span data-ttu-id="44fa3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44fa3-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="44fa3-112">Elenca le chiavi dell'account Dieresdb.</span><span class="sxs-lookup"><span data-stu-id="44fa3-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="44fa3-113">Il tipo di chiave può essere un valore compreso tra: ConnectionStrings, Keys e ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="44fa3-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="44fa3-114">L'impostazione predefinita è Chiavi.</span><span class="sxs-lookup"><span data-stu-id="44fa3-114">Default is Keys.</span></span>

## <span data-ttu-id="44fa3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44fa3-115">PARAMETERS</span></span>

### <span data-ttu-id="44fa3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fa3-116">-DefaultProfile</span></span>
<span data-ttu-id="44fa3-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44fa3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fa3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44fa3-118">-InputObject</span></span>
<span data-ttu-id="44fa3-119">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="44fa3-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="44fa3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="44fa3-120">-Name</span></span>
<span data-ttu-id="44fa3-121">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="44fa3-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="44fa3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fa3-122">-ResourceGroupName</span></span>
<span data-ttu-id="44fa3-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44fa3-123">Name of resource group.</span></span>

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

### <span data-ttu-id="44fa3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44fa3-124">-ResourceId</span></span>
<span data-ttu-id="44fa3-125">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="44fa3-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="44fa3-126">-Type</span><span class="sxs-lookup"><span data-stu-id="44fa3-126">-Type</span></span>
<span data-ttu-id="44fa3-127">Valore da: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="44fa3-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="44fa3-128">L'impostazione predefinita è Chiavi.</span><span class="sxs-lookup"><span data-stu-id="44fa3-128">Default is Keys.</span></span>

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

### <span data-ttu-id="44fa3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fa3-129">CommonParameters</span></span>
<span data-ttu-id="44fa3-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fa3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fa3-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44fa3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fa3-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="44fa3-132">INPUTS</span></span>

### <span data-ttu-id="44fa3-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="44fa3-133">None</span></span>

## <span data-ttu-id="44fa3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44fa3-134">OUTPUTS</span></span>

### <span data-ttu-id="44fa3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="44fa3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="44fa3-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="44fa3-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="44fa3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="44fa3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="44fa3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="44fa3-138">NOTES</span></span>

## <span data-ttu-id="44fa3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44fa3-139">RELATED LINKS</span></span>
