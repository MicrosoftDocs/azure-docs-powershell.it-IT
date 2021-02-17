---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196543"
---
# <span data-ttu-id="48ee4-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="48ee4-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="48ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="48ee4-103">Crea un'impostazione di database per la migrazione di mongoDb</span><span class="sxs-lookup"><span data-stu-id="48ee4-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="48ee4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48ee4-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="48ee4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="48ee4-106">Il New-AzDataMigrationMongoDbDatabaseSetting cmdlet crea l'oggetto delle impostazioni di migrazione che specifica la velocità effettiva e il comportamento di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="48ee4-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="48ee4-107">L'output è una coppia di valori chiave con il nome della raccolta e il valore dell'impostazione, che può essere usata per richiamare l'attività di migrazione.</span><span class="sxs-lookup"><span data-stu-id="48ee4-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="48ee4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48ee4-108">EXAMPLES</span></span>

### <span data-ttu-id="48ee4-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48ee4-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="48ee4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="48ee4-111">-Name</span><span class="sxs-lookup"><span data-stu-id="48ee4-111">-Name</span></span>
<span data-ttu-id="48ee4-112">Nome del database</span><span class="sxs-lookup"><span data-stu-id="48ee4-112">Name of the database</span></span>

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
### <span data-ttu-id="48ee4-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="48ee4-113">-TargetRequestUnit</span></span>
<span data-ttu-id="48ee4-114">Valore di unità di richiesta a livello di database dedicato.</span><span class="sxs-lookup"><span data-stu-id="48ee4-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="48ee4-115">Se non è impostata, la raccolta usa il database condiviso RU.</span><span class="sxs-lookup"><span data-stu-id="48ee4-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="48ee4-116">-Raccolte</span><span class="sxs-lookup"><span data-stu-id="48ee4-116">-Collections</span></span>
<span data-ttu-id="48ee4-117">Matrice degli oggetti delle impostazioni della raccolta MongoDb restituiti dalla New-AzureRmDmsMongoDbDatabaseSetting chiamata.</span><span class="sxs-lookup"><span data-stu-id="48ee4-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="48ee4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ee4-118">CommonParameters</span></span>
<span data-ttu-id="48ee4-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ee4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ee4-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ee4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ee4-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="48ee4-121">INPUTS</span></span>

### <span data-ttu-id="48ee4-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="48ee4-122">None</span></span>

## <span data-ttu-id="48ee4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48ee4-123">OUTPUTS</span></span>

### <span data-ttu-id="48ee4-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="48ee4-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="48ee4-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="48ee4-125">NOTES</span></span>

## <span data-ttu-id="48ee4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48ee4-126">RELATED LINKS</span></span>
