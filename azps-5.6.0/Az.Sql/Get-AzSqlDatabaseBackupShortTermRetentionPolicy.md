---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 4cb97982ed3649502bcf11ce471cef0231ae3058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967502"
---
# <span data-ttu-id="669a9-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="669a9-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="669a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669a9-102">SYNOPSIS</span></span>
<span data-ttu-id="669a9-103">Ottiene un criterio di conservazione a breve termine di backup.</span><span class="sxs-lookup"><span data-stu-id="669a9-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="669a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="669a9-104">SYNTAX</span></span>

### <span data-ttu-id="669a9-105">PolicyByResourceServerDatabaseSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="669a9-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="669a9-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="669a9-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="669a9-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="669a9-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="669a9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="669a9-108">DESCRIPTION</span></span>
<span data-ttu-id="669a9-109">Il cmdlet **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** ottiene il criterio di conservazione a breve termine registrato nel database.</span><span class="sxs-lookup"><span data-stu-id="669a9-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="669a9-110">Il criterio è il periodo di conservazione, in giorni, per i backup di ripristino tempormente pianificati.</span><span class="sxs-lookup"><span data-stu-id="669a9-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="669a9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="669a9-111">EXAMPLES</span></span>

### <span data-ttu-id="669a9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="669a9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="669a9-113">Questo comando ottiene i criteri di conservazione a breve termine per database01.</span><span class="sxs-lookup"><span data-stu-id="669a9-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="669a9-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="669a9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="669a9-115">Questo comando recupera i criteri di conservazione a breve termine per database01 tramite piping in un oggetto di database.</span><span class="sxs-lookup"><span data-stu-id="669a9-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="669a9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="669a9-116">PARAMETERS</span></span>

### <span data-ttu-id="669a9-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="669a9-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="669a9-118">Oggetto di database per cui ottenere i criteri.</span><span class="sxs-lookup"><span data-stu-id="669a9-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="669a9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="669a9-119">-DatabaseName</span></span>
<span data-ttu-id="669a9-120">Il nome del database SQL Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="669a9-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669a9-121">-DefaultProfile</span></span>
<span data-ttu-id="669a9-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="669a9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="669a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="669a9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="669a9-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="669a9-125">-ResourceId</span></span>
<span data-ttu-id="669a9-126">ID risorsa per i criteri di conservazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="669a9-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669a9-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="669a9-127">-ServerName</span></span>
<span data-ttu-id="669a9-128">Nome della cartella di SQL Server Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="669a9-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669a9-129">CommonParameters</span></span>
<span data-ttu-id="669a9-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669a9-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="669a9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669a9-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="669a9-132">INPUTS</span></span>

### <span data-ttu-id="669a9-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="669a9-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="669a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="669a9-134">System.String</span></span>

## <span data-ttu-id="669a9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="669a9-135">OUTPUTS</span></span>

### <span data-ttu-id="669a9-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="669a9-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="669a9-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="669a9-137">NOTES</span></span>

## <span data-ttu-id="669a9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="669a9-138">RELATED LINKS</span></span>
