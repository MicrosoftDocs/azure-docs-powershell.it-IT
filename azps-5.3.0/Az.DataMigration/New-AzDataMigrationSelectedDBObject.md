---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377649"
---
# <span data-ttu-id="1c4cd-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="1c4cd-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="1c4cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4cd-103">Crea un oggetto di input del database che contiene informazioni sui database di origine e di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="1c4cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c4cd-104">SYNTAX</span></span>

### <span data-ttu-id="1c4cd-105">MigrateSqlServerSqlDb (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c4cd-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4cd-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="1c4cd-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c4cd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c4cd-107">DESCRIPTION</span></span>
<span data-ttu-id="1c4cd-108">Il cmdlet New-AzDataMigrationSelectedDB crea un oggetto info database che contiene informazioni sui database di origine e di destinazione, oltre ai mapping delle tabelle, per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="1c4cd-109">Questo cmdlet può essere usato come parametro con il cmdlet New-AzDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="1c4cd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c4cd-110">EXAMPLES</span></span>

### <span data-ttu-id="1c4cd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c4cd-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="1c4cd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1c4cd-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="1c4cd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c4cd-113">PARAMETERS</span></span>

### <span data-ttu-id="1c4cd-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="1c4cd-114">-BackupFileShare</span></span>
<span data-ttu-id="1c4cd-115">Condivisione file in cui è necessario eseguire il backup dei file di database del server di origine per il database.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="1c4cd-116">Usare questa impostazione per ignorare le informazioni sulla condivisione di file per ogni database.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="1c4cd-117">Usare il nome di dominio completo per il server.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="1c4cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4cd-118">-DefaultProfile</span></span>
<span data-ttu-id="1c4cd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4cd-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="1c4cd-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="1c4cd-121">Impostare il database in ReadOnly prima della migrazione</span><span class="sxs-lookup"><span data-stu-id="1c4cd-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="1c4cd-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="1c4cd-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="1c4cd-123">Impostare il tipo di migrazione su SQL Server per la migrazione a SQL DB.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="1c4cd-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="1c4cd-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="1c4cd-125">Impostare il tipo di migrazione su SQL Server su SQL DB MI Migration.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="1c4cd-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c4cd-126">-SourceDatabaseName</span></span>
<span data-ttu-id="1c4cd-127">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-127">The name of the source database.</span></span>

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

### <span data-ttu-id="1c4cd-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="1c4cd-128">-TableMap</span></span>
<span data-ttu-id="1c4cd-129">mapping dell'origine alle tabelle di destinazione</span><span class="sxs-lookup"><span data-stu-id="1c4cd-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="1c4cd-130">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="1c4cd-130">-TargetDatabaseName</span></span>
<span data-ttu-id="1c4cd-131">Nome del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-131">The name of the target database.</span></span>

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

### <span data-ttu-id="1c4cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4cd-132">CommonParameters</span></span>
<span data-ttu-id="1c4cd-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4cd-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4cd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4cd-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c4cd-135">INPUTS</span></span>

### <span data-ttu-id="1c4cd-136">Microsoft. Azure. Management. DataMigration. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="1c4cd-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="1c4cd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c4cd-137">OUTPUTS</span></span>

### <span data-ttu-id="1c4cd-138">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="1c4cd-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="1c4cd-139">Note</span><span class="sxs-lookup"><span data-stu-id="1c4cd-139">NOTES</span></span>

## <span data-ttu-id="1c4cd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c4cd-140">RELATED LINKS</span></span>
