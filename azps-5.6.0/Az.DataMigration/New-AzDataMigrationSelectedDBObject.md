---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: c6e417ade1e411eaaa0b86f8f69ac6c17f228e91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998044"
---
# <span data-ttu-id="14cbb-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="14cbb-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="14cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="14cbb-103">Crea un oggetto di input di database che contiene informazioni sui database di origine e di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="14cbb-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="14cbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14cbb-104">SYNTAX</span></span>

### <span data-ttu-id="14cbb-105">MigrateSqlServerSqlDb (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14cbb-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14cbb-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="14cbb-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14cbb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="14cbb-108">Il cmdlet New-AzDataMigrationSelectedDB crea un oggetto informazioni di database contenente informazioni sui database di origine e di destinazione, nonché i mapping di tabella, per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="14cbb-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="14cbb-109">Questo cmdlet può essere usato come parametro con il cmdlet New-AzDataMigrationTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14cbb-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="14cbb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14cbb-110">EXAMPLES</span></span>

### <span data-ttu-id="14cbb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14cbb-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="14cbb-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="14cbb-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="14cbb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14cbb-113">PARAMETERS</span></span>

### <span data-ttu-id="14cbb-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="14cbb-114">-BackupFileShare</span></span>
<span data-ttu-id="14cbb-115">Condivisione file in cui eseguire il backup dei file di database del server di origine per il database.</span><span class="sxs-lookup"><span data-stu-id="14cbb-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="14cbb-116">Usare questa impostazione per ignorare le informazioni sulla condivisione file per ogni database.</span><span class="sxs-lookup"><span data-stu-id="14cbb-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="14cbb-117">Usare il nome di dominio completo per il server.</span><span class="sxs-lookup"><span data-stu-id="14cbb-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="14cbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14cbb-118">-DefaultProfile</span></span>
<span data-ttu-id="14cbb-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14cbb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14cbb-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="14cbb-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="14cbb-121">Impostare il database su readonly prima della migrazione</span><span class="sxs-lookup"><span data-stu-id="14cbb-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="14cbb-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="14cbb-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="14cbb-123">Impostare il tipo di migrazione SQL Server migrazione SQL a DB.</span><span class="sxs-lookup"><span data-stu-id="14cbb-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="14cbb-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="14cbb-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="14cbb-125">Impostare il tipo di migrazione SQL Server per SQL migrazione MI di DB.</span><span class="sxs-lookup"><span data-stu-id="14cbb-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="14cbb-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="14cbb-126">-SourceDatabaseName</span></span>
<span data-ttu-id="14cbb-127">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="14cbb-127">The name of the source database.</span></span>

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

### <span data-ttu-id="14cbb-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="14cbb-128">-TableMap</span></span>
<span data-ttu-id="14cbb-129">Mapping tra tabelle di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="14cbb-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="14cbb-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="14cbb-130">-TargetDatabaseName</span></span>
<span data-ttu-id="14cbb-131">Nome del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14cbb-131">The name of the target database.</span></span>

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

### <span data-ttu-id="14cbb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cbb-132">CommonParameters</span></span>
<span data-ttu-id="14cbb-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14cbb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14cbb-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14cbb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cbb-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="14cbb-135">INPUTS</span></span>

### <span data-ttu-id="14cbb-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="14cbb-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="14cbb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14cbb-137">OUTPUTS</span></span>

### <span data-ttu-id="14cbb-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="14cbb-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="14cbb-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="14cbb-139">NOTES</span></span>

## <span data-ttu-id="14cbb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14cbb-140">RELATED LINKS</span></span>
