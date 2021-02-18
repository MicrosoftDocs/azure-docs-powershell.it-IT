---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180895"
---
# <span data-ttu-id="0b04b-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="0b04b-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="0b04b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b04b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b04b-103">Crea un'impostazione di raccolta per la migrazione in base alla migrazione mongoDb</span><span class="sxs-lookup"><span data-stu-id="0b04b-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="0b04b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b04b-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="0b04b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b04b-105">DESCRIPTION</span></span>
<span data-ttu-id="0b04b-106">Il New-AzDataMigrationMongoDbCollectionSetting cmdlet crea l'oggetto delle impostazioni di migrazione che specifica la velocità effettiva e il comportamento di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="0b04b-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="0b04b-107">L'output del cmdlet è una coppia di valori chiave con il nome della raccolta e il valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="0b04b-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="0b04b-108">L'output viene usato nell'assemblaggio delle impostazioni a livello di database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0b04b-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="0b04b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b04b-109">EXAMPLES</span></span>

### <span data-ttu-id="0b04b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b04b-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="0b04b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b04b-111">PARAMETERS</span></span>

### <span data-ttu-id="0b04b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="0b04b-112">-Name</span></span>
<span data-ttu-id="0b04b-113">Nome della raccolta</span><span class="sxs-lookup"><span data-stu-id="0b04b-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b04b-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="0b04b-114">-ShardKey</span></span>
<span data-ttu-id="0b04b-115">Elenco separato da virgole delle chiavi partizionate.</span><span class="sxs-lookup"><span data-stu-id="0b04b-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="0b04b-116">Per la destinazione mongoDb, è possibile specificare l'ordine della chiave shard di "ShardKeyName:Order", dove order è 1, -1 o vuoto per l'hashing, ad esempio "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="0b04b-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b04b-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="0b04b-117">-TargetRequestUnit</span></span>
<span data-ttu-id="0b04b-118">Valore di unità di richiesta di raccolta dedicato.</span><span class="sxs-lookup"><span data-stu-id="0b04b-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="0b04b-119">Se non è impostata, la raccolta usa il database condiviso RU.</span><span class="sxs-lookup"><span data-stu-id="0b04b-119">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b04b-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="0b04b-120">-CanDelete</span></span>
<span data-ttu-id="0b04b-121">Se i dati di destinazione devono essere eliminati, se l'opzione è impostata, verrà cancellata durante la migrazione</span><span class="sxs-lookup"><span data-stu-id="0b04b-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="0b04b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b04b-122">CommonParameters</span></span>
<span data-ttu-id="0b04b-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b04b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b04b-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b04b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b04b-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b04b-125">INPUTS</span></span>

### <span data-ttu-id="0b04b-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b04b-126">None</span></span>

## <span data-ttu-id="0b04b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b04b-127">OUTPUTS</span></span>

### <span data-ttu-id="0b04b-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="0b04b-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="0b04b-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b04b-129">NOTES</span></span>

## <span data-ttu-id="0b04b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b04b-130">RELATED LINKS</span></span>
