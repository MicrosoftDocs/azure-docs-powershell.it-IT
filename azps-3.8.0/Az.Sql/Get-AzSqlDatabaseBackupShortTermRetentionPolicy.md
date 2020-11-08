---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019515"
---
# <span data-ttu-id="5501e-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5501e-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="5501e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5501e-102">SYNOPSIS</span></span>
<span data-ttu-id="5501e-103">Ottiene un criterio di conservazione a breve termine di backup.</span><span class="sxs-lookup"><span data-stu-id="5501e-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="5501e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5501e-104">SYNTAX</span></span>

### <span data-ttu-id="5501e-105">PolicyByResourceServerDatabaseSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5501e-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5501e-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5501e-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5501e-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5501e-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5501e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5501e-108">DESCRIPTION</span></span>
<span data-ttu-id="5501e-109">Il cmdlet **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** ottiene i criteri di conservazione a breve termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="5501e-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="5501e-110">Il criterio è il periodo di conservazione, in giorni, per i backup di ripristino temporizzato.</span><span class="sxs-lookup"><span data-stu-id="5501e-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="5501e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5501e-111">EXAMPLES</span></span>

### <span data-ttu-id="5501e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5501e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="5501e-113">Questo comando ottiene i criteri di conservazione a breve termine per Database01.</span><span class="sxs-lookup"><span data-stu-id="5501e-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="5501e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5501e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="5501e-115">Questo comando consente di ottenere i criteri di conservazione a breve termine per Database01 tramite piping in un oggetto di database.</span><span class="sxs-lookup"><span data-stu-id="5501e-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="5501e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5501e-116">PARAMETERS</span></span>

### <span data-ttu-id="5501e-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5501e-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="5501e-118">Oggetto database per cui ottenere i criteri.</span><span class="sxs-lookup"><span data-stu-id="5501e-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="5501e-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5501e-119">-DatabaseName</span></span>
<span data-ttu-id="5501e-120">Nome del database SQL di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="5501e-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="5501e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5501e-121">-DefaultProfile</span></span>
<span data-ttu-id="5501e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5501e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5501e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5501e-123">-ResourceGroupName</span></span>
<span data-ttu-id="5501e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5501e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5501e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5501e-125">-ResourceId</span></span>
<span data-ttu-id="5501e-126">ID risorsa dei criteri di conservazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="5501e-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="5501e-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5501e-127">-ServerName</span></span>
<span data-ttu-id="5501e-128">Il nome di Azure SQL Server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="5501e-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="5501e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5501e-129">CommonParameters</span></span>
<span data-ttu-id="5501e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5501e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5501e-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5501e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5501e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5501e-132">INPUTS</span></span>

### <span data-ttu-id="5501e-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5501e-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="5501e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5501e-134">System.String</span></span>

## <span data-ttu-id="5501e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5501e-135">OUTPUTS</span></span>

### <span data-ttu-id="5501e-136">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5501e-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="5501e-137">Note</span><span class="sxs-lookup"><span data-stu-id="5501e-137">NOTES</span></span>

## <span data-ttu-id="5501e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5501e-138">RELATED LINKS</span></span>
