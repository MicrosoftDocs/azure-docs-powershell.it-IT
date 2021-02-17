---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180871"
---
# <span data-ttu-id="e12d6-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e12d6-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="e12d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e12d6-103">Crea un oggetto informazioni di database specifico dello scenario di sincronizzazione da usare per un'attività di migrazione.</span><span class="sxs-lookup"><span data-stu-id="e12d6-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="e12d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e12d6-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e12d6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e12d6-105">DESCRIPTION</span></span>

<span data-ttu-id="e12d6-106">Il New-AzDataMigrationSyncSelectedDB cmdlet crea un oggetto informazioni di database specifico dello scenario di sincronizzazione che contiene informazioni sui database di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e12d6-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="e12d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e12d6-107">EXAMPLES</span></span>

### <span data-ttu-id="e12d6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e12d6-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="e12d6-109">Questo esempio crea un oggetto metadati di database che descrive le impostazioni di migrazione $DatabaseName al database $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="e12d6-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="e12d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e12d6-110">PARAMETERS</span></span>

### <span data-ttu-id="e12d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12d6-111">-DefaultProfile</span></span>
<span data-ttu-id="e12d6-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e12d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12d6-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="e12d6-113">-MigrationSetting</span></span>
<span data-ttu-id="e12d6-114">Impostazioni di migrazione che regolano il comportamento della migrazione</span><span class="sxs-lookup"><span data-stu-id="e12d6-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="e12d6-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e12d6-115">-SchemaName</span></span>
<span data-ttu-id="e12d6-116">Nome dello schema di cui eseguire la migrazione</span><span class="sxs-lookup"><span data-stu-id="e12d6-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="e12d6-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e12d6-117">-SourceDatabaseName</span></span>
<span data-ttu-id="e12d6-118">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="e12d6-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12d6-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="e12d6-119">-SourceSetting</span></span>
<span data-ttu-id="e12d6-120">Impostazioni di origine per ottimizzare il comportamento di migrazione dell'endpoint di origine</span><span class="sxs-lookup"><span data-stu-id="e12d6-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="e12d6-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="e12d6-121">-TableMap</span></span>
<span data-ttu-id="e12d6-122">Mapping tra tabelle di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="e12d6-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="e12d6-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e12d6-123">-TargetDatabaseName</span></span>
<span data-ttu-id="e12d6-124">Nome del database di destinazione</span><span class="sxs-lookup"><span data-stu-id="e12d6-124">The name of the target database</span></span>

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

### <span data-ttu-id="e12d6-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="e12d6-125">-TargetSetting</span></span>
<span data-ttu-id="e12d6-126">Impostazioni di destinazione per ottimizzare il comportamento di migrazione dell'endpoint di destinazione</span><span class="sxs-lookup"><span data-stu-id="e12d6-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="e12d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12d6-127">CommonParameters</span></span>
<span data-ttu-id="e12d6-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12d6-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e12d6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12d6-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="e12d6-130">INPUTS</span></span>

### <span data-ttu-id="e12d6-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e12d6-131">None</span></span>

## <span data-ttu-id="e12d6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e12d6-132">OUTPUTS</span></span>

### <span data-ttu-id="e12d6-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="e12d6-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="e12d6-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="e12d6-134">NOTES</span></span>

## <span data-ttu-id="e12d6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e12d6-135">RELATED LINKS</span></span>
