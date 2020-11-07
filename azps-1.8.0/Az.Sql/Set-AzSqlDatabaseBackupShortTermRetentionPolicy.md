---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ac63ae50893ec54a2d14431c55229fad71c80c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676757"
---
# <span data-ttu-id="e5db9-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5db9-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="e5db9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5db9-102">SYNOPSIS</span></span>
<span data-ttu-id="e5db9-103">Imposta un criterio di conservazione a breve termine per il backup.</span><span class="sxs-lookup"><span data-stu-id="e5db9-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="e5db9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5db9-104">SYNTAX</span></span>

### <span data-ttu-id="e5db9-105">PolicyByResourceServerDatabaseSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5db9-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5db9-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5db9-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5db9-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5db9-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5db9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5db9-108">DESCRIPTION</span></span>
<span data-ttu-id="e5db9-109">Il cmdlet **set-AzSqlDatabaseBackupShortTermRetentionPolicy** ottiene i criteri di conservazione a breve termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="e5db9-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="e5db9-110">Il criterio è il periodo di conservazione, in giorni, per i backup di ripristino temporizzato.</span><span class="sxs-lookup"><span data-stu-id="e5db9-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="e5db9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5db9-111">EXAMPLES</span></span>

### <span data-ttu-id="e5db9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5db9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="e5db9-113">Questo comando imposta i criteri di conservazione a breve termine per Database01 in 35 giorni.</span><span class="sxs-lookup"><span data-stu-id="e5db9-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="e5db9-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e5db9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="e5db9-115">Questo comando imposta i criteri di conservazione a breve termine per Database01 in 35 giorni tramite piping in un oggetto di database.</span><span class="sxs-lookup"><span data-stu-id="e5db9-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="e5db9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5db9-116">PARAMETERS</span></span>

### <span data-ttu-id="e5db9-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e5db9-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="e5db9-118">Oggetto database per cui ottenere i criteri.</span><span class="sxs-lookup"><span data-stu-id="e5db9-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="e5db9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5db9-119">-DatabaseName</span></span>
<span data-ttu-id="e5db9-120">Nome del database SQL di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="e5db9-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="e5db9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5db9-121">-DefaultProfile</span></span>
<span data-ttu-id="e5db9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5db9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5db9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5db9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5db9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5db9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5db9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5db9-125">-ResourceId</span></span>
<span data-ttu-id="e5db9-126">ID risorsa dei criteri di conservazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="e5db9-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="e5db9-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="e5db9-127">-RetentionDays</span></span>
<span data-ttu-id="e5db9-128">Impostazione di conservazione del backup in giorni.</span><span class="sxs-lookup"><span data-stu-id="e5db9-128">The backup retention setting, in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db9-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e5db9-129">-ServerName</span></span>
<span data-ttu-id="e5db9-130">Il nome di Azure SQL Server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="e5db9-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="e5db9-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5db9-131">-Confirm</span></span>
<span data-ttu-id="e5db9-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5db9-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5db9-133">-WhatIf</span></span>
<span data-ttu-id="e5db9-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5db9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5db9-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5db9-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5db9-136">CommonParameters</span></span>
<span data-ttu-id="e5db9-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5db9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5db9-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5db9-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5db9-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5db9-139">INPUTS</span></span>

### <span data-ttu-id="e5db9-140">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e5db9-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="e5db9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e5db9-141">System.String</span></span>

## <span data-ttu-id="e5db9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5db9-142">OUTPUTS</span></span>

### <span data-ttu-id="e5db9-143">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e5db9-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="e5db9-144">Note</span><span class="sxs-lookup"><span data-stu-id="e5db9-144">NOTES</span></span>

## <span data-ttu-id="e5db9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5db9-145">RELATED LINKS</span></span>