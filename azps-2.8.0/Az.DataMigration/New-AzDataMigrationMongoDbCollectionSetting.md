---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 041f67940fbe79a751b969dd17223f453f4929d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674730"
---
# <span data-ttu-id="96c25-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="96c25-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="96c25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96c25-102">SYNOPSIS</span></span>
<span data-ttu-id="96c25-103">Crea l'impostazione della raccolta per la migrazione in base alla migrazione mongoDb</span><span class="sxs-lookup"><span data-stu-id="96c25-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="96c25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96c25-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="96c25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96c25-105">DESCRIPTION</span></span>
<span data-ttu-id="96c25-106">Il cmdlet New-AzDataMigrationMongoDbCollectionSetting crea l'oggetto delle impostazioni di migrazione che specifica il comportamento di eliminazione e velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="96c25-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="96c25-107">Output il cmdlet è una coppia di valori chiave con il nome della raccolta e il valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="96c25-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="96c25-108">L'output viene usato per assemblare le impostazioni del livello di database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="96c25-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="96c25-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96c25-109">EXAMPLES</span></span>

### <span data-ttu-id="96c25-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96c25-110">Example 1</span></span>
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

## <span data-ttu-id="96c25-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96c25-111">PARAMETERS</span></span>

### <span data-ttu-id="96c25-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="96c25-112">-Name</span></span>
<span data-ttu-id="96c25-113">Nome della raccolta</span><span class="sxs-lookup"><span data-stu-id="96c25-113">Name of the collection</span></span>

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

### <span data-ttu-id="96c25-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="96c25-114">-ShardKey</span></span>
<span data-ttu-id="96c25-115">Elenco separato da virgole delle chiavi di frammento.</span><span class="sxs-lookup"><span data-stu-id="96c25-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="96c25-116">Per la destinazione mongoDb, è possibile specificare l'ordine di chiave di frammentazione "ShardKeyName: Order", dove Order è 1,-1 o Empty per Hashed, ad esempio "_id, posta elettronica:-1".</span><span class="sxs-lookup"><span data-stu-id="96c25-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="96c25-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="96c25-117">-TargetRequestUnit</span></span>
<span data-ttu-id="96c25-118">Valore unitario di richiesta di raccolta dedicato.</span><span class="sxs-lookup"><span data-stu-id="96c25-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="96c25-119">Se non è impostata, tale raccolta usa il database condiviso RU.</span><span class="sxs-lookup"><span data-stu-id="96c25-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="96c25-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="96c25-120">-CanDelete</span></span>
<span data-ttu-id="96c25-121">Se si suppone che i dati di destinazione vengano eliminati, se l'opzione è impostata, verrà pulita alla migrazione</span><span class="sxs-lookup"><span data-stu-id="96c25-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="96c25-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c25-122">CommonParameters</span></span>
<span data-ttu-id="96c25-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c25-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c25-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c25-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c25-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96c25-125">INPUTS</span></span>

### <span data-ttu-id="96c25-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96c25-126">None</span></span>

## <span data-ttu-id="96c25-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96c25-127">OUTPUTS</span></span>

### <span data-ttu-id="96c25-128">Microsoft. Azure. Commands. DataMigration. Models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="96c25-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="96c25-129">Note</span><span class="sxs-lookup"><span data-stu-id="96c25-129">NOTES</span></span>

## <span data-ttu-id="96c25-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96c25-130">RELATED LINKS</span></span>
