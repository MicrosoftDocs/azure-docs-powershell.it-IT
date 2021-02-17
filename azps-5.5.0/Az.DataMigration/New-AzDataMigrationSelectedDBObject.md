---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177070"
---
# <span data-ttu-id="9cf93-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="9cf93-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="9cf93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cf93-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf93-103">Crea un oggetto di input di database che contiene informazioni sui database di origine e di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="9cf93-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="9cf93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cf93-104">SYNTAX</span></span>

### <span data-ttu-id="9cf93-105">MigrateSqlServerSqlDb (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cf93-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cf93-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="9cf93-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf93-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9cf93-107">DESCRIPTION</span></span>
<span data-ttu-id="9cf93-108">Il cmdlet New-AzDataMigrationSelectedDB crea un oggetto informazioni di database contenente informazioni sui database di origine e di destinazione, nonché i mapping di tabella, per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="9cf93-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="9cf93-109">Questo cmdlet può essere usato come parametro con il cmdlet New-AzDataMigrationTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cf93-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="9cf93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cf93-110">EXAMPLES</span></span>

### <span data-ttu-id="9cf93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9cf93-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="9cf93-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9cf93-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="9cf93-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cf93-113">PARAMETERS</span></span>

### <span data-ttu-id="9cf93-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="9cf93-114">-BackupFileShare</span></span>
<span data-ttu-id="9cf93-115">Condivisione file in cui eseguire il backup dei file di database del server di origine per il database.</span><span class="sxs-lookup"><span data-stu-id="9cf93-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="9cf93-116">Usare questa impostazione per ignorare le informazioni sulla condivisione file per ogni database.</span><span class="sxs-lookup"><span data-stu-id="9cf93-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="9cf93-117">Usare il nome di dominio completo per il server.</span><span class="sxs-lookup"><span data-stu-id="9cf93-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf93-118">-DefaultProfile</span></span>
<span data-ttu-id="9cf93-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf93-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cf93-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="9cf93-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="9cf93-121">Impostare il database su ReadOnly prima della migrazione</span><span class="sxs-lookup"><span data-stu-id="9cf93-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf93-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="9cf93-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="9cf93-123">Impostare il tipo di migrazione SQL Server per SQL a DB.</span><span class="sxs-lookup"><span data-stu-id="9cf93-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf93-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="9cf93-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="9cf93-125">Impostare il tipo di migrazione SQL Server per SQL migrazione MI di DB.</span><span class="sxs-lookup"><span data-stu-id="9cf93-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf93-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="9cf93-126">-SourceDatabaseName</span></span>
<span data-ttu-id="9cf93-127">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="9cf93-127">The name of the source database.</span></span>

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

### <span data-ttu-id="9cf93-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="9cf93-128">-TableMap</span></span>
<span data-ttu-id="9cf93-129">Mapping tra tabelle di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="9cf93-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf93-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="9cf93-130">-TargetDatabaseName</span></span>
<span data-ttu-id="9cf93-131">Nome del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9cf93-131">The name of the target database.</span></span>

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

### <span data-ttu-id="9cf93-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf93-132">CommonParameters</span></span>
<span data-ttu-id="9cf93-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf93-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf93-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf93-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf93-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="9cf93-135">INPUTS</span></span>

### <span data-ttu-id="9cf93-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="9cf93-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="9cf93-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cf93-137">OUTPUTS</span></span>

### <span data-ttu-id="9cf93-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="9cf93-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="9cf93-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="9cf93-139">NOTES</span></span>

## <span data-ttu-id="9cf93-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cf93-140">RELATED LINKS</span></span>
