---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387547"
---
# <span data-ttu-id="2cc5c-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="2cc5c-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="2cc5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc5c-103">Crea l'impostazione di database per la migrazione per la migrazione mongoDb</span><span class="sxs-lookup"><span data-stu-id="2cc5c-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="2cc5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cc5c-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="2cc5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc5c-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc5c-106">Il cmdlet New-AzDataMigrationMongoDbDatabaseSetting crea l'oggetto delle impostazioni di migrazione che specifica il comportamento di eliminazione e velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="2cc5c-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="2cc5c-107">L'output è una coppia di valori chiave con il nome della raccolta e il valore dell'impostazione, che può essere usata per richiamare l'attività di migrazione.</span><span class="sxs-lookup"><span data-stu-id="2cc5c-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="2cc5c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cc5c-108">EXAMPLES</span></span>

### <span data-ttu-id="2cc5c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cc5c-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="2cc5c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cc5c-110">PARAMETERS</span></span>

### <span data-ttu-id="2cc5c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cc5c-111">-Name</span></span>
<span data-ttu-id="2cc5c-112">Nome del database</span><span class="sxs-lookup"><span data-stu-id="2cc5c-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="2cc5c-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="2cc5c-113">-TargetRequestUnit</span></span>
<span data-ttu-id="2cc5c-114">Valore dell'unità di richiesta livello database dedicato.</span><span class="sxs-lookup"><span data-stu-id="2cc5c-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="2cc5c-115">Se non è impostata, tale raccolta usa il database condiviso RU.</span><span class="sxs-lookup"><span data-stu-id="2cc5c-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="2cc5c-116">-Raccolte</span><span class="sxs-lookup"><span data-stu-id="2cc5c-116">-Collections</span></span>
<span data-ttu-id="2cc5c-117">Matrice di oggetti setting della raccolta MongoDb restituiti da New-AzureRmDmsMongoDbDatabaseSetting chiamata.</span><span class="sxs-lookup"><span data-stu-id="2cc5c-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc5c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc5c-118">CommonParameters</span></span>
<span data-ttu-id="2cc5c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc5c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc5c-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc5c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc5c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cc5c-121">INPUTS</span></span>

### <span data-ttu-id="2cc5c-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2cc5c-122">None</span></span>

## <span data-ttu-id="2cc5c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cc5c-123">OUTPUTS</span></span>

### <span data-ttu-id="2cc5c-124">Microsoft. Azure. Commands. DataMigration. Models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="2cc5c-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="2cc5c-125">Note</span><span class="sxs-lookup"><span data-stu-id="2cc5c-125">NOTES</span></span>

## <span data-ttu-id="2cc5c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cc5c-126">RELATED LINKS</span></span>
