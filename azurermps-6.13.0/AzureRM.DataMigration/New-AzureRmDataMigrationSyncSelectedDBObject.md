---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: fc400c9eeb64acfa081d5a60a5e65089f415817b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687601"
---
# <span data-ttu-id="e36dc-101">New-AzureRmDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e36dc-101">New-AzureRmDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="e36dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e36dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e36dc-103">Crea un oggetto info database specifico dello scenario di sincronizzazione da usare per un'attività di migrazione.</span><span class="sxs-lookup"><span data-stu-id="e36dc-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e36dc-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String>
 -TableMap <Hashtable> [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>]
 [-TargetSetting <Hashtable>] -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e36dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e36dc-105">DESCRIPTION</span></span>

<span data-ttu-id="e36dc-106">Il cmdlet New-AzureRmDataMigrationSyncSelectedDB crea un oggetto info database specifico dello scenario di sincronizzazione che contiene informazioni sui database di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e36dc-106">The New-AzureRmDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="e36dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e36dc-107">EXAMPLES</span></span>

### <span data-ttu-id="e36dc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e36dc-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzureRmDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="e36dc-109">Questo esempio crea un oggetto metadati di database che descrive le impostazioni di migrazione per $DatabaseName $DatabaseName di database.</span><span class="sxs-lookup"><span data-stu-id="e36dc-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="e36dc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e36dc-110">PARAMETERS</span></span>

### <span data-ttu-id="e36dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36dc-111">-DefaultProfile</span></span>
<span data-ttu-id="e36dc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e36dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="e36dc-113">-MigrationSetting</span></span>
<span data-ttu-id="e36dc-114">Impostazioni di migrazione che ottimizzano il comportamento di migrazione</span><span class="sxs-lookup"><span data-stu-id="e36dc-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e36dc-115">-SchemaName</span></span>
<span data-ttu-id="e36dc-116">Nome dello schema di cui eseguire la migrazione</span><span class="sxs-lookup"><span data-stu-id="e36dc-116">Schema name to be migrated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e36dc-117">-SourceDatabaseName</span></span>
<span data-ttu-id="e36dc-118">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="e36dc-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="e36dc-119">-SourceSetting</span></span>
<span data-ttu-id="e36dc-120">Impostazioni di origine per ottimizzare il comportamento della migrazione di endpoint di origine</span><span class="sxs-lookup"><span data-stu-id="e36dc-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="e36dc-121">-TableMap</span></span>
<span data-ttu-id="e36dc-122">Mapping dell'origine alle tabelle di destinazione</span><span class="sxs-lookup"><span data-stu-id="e36dc-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-123">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="e36dc-123">-TargetDatabaseName</span></span>
<span data-ttu-id="e36dc-124">Nome del database di destinazione</span><span class="sxs-lookup"><span data-stu-id="e36dc-124">The name of the target database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="e36dc-125">-TargetSetting</span></span>
<span data-ttu-id="e36dc-126">Impostazioni di destinazione per ottimizzare il comportamento di migrazione degli endpoint di destinazione</span><span class="sxs-lookup"><span data-stu-id="e36dc-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36dc-127">CommonParameters</span></span>
<span data-ttu-id="e36dc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36dc-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36dc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e36dc-130">INPUTS</span></span>

### <span data-ttu-id="e36dc-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e36dc-131">None</span></span>

## <span data-ttu-id="e36dc-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e36dc-132">OUTPUTS</span></span>

### <span data-ttu-id="e36dc-133">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="e36dc-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="e36dc-134">Note</span><span class="sxs-lookup"><span data-stu-id="e36dc-134">NOTES</span></span>

## <span data-ttu-id="e36dc-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e36dc-135">RELATED LINKS</span></span>
