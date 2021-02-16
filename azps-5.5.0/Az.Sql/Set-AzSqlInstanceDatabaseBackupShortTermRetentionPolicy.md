---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176742"
---
# <span data-ttu-id="76921-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76921-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="76921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76921-102">SYNOPSIS</span></span>
<span data-ttu-id="76921-103">Imposta un criterio di conservazione a breve termine per il backup.</span><span class="sxs-lookup"><span data-stu-id="76921-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="76921-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76921-104">SYNTAX</span></span>

### <span data-ttu-id="76921-105">PolicyByResourceInstanceDatabaseSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76921-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76921-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76921-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76921-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="76921-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76921-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76921-108">DESCRIPTION</span></span>
<span data-ttu-id="76921-109">Il cmdlet **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** ottiene il criterio di conservazione a breve termine registrato nel database.</span><span class="sxs-lookup"><span data-stu-id="76921-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="76921-110">Il criterio è il periodo di conservazione, in giorni, per i backup di ripristino tempormente pianificati.</span><span class="sxs-lookup"><span data-stu-id="76921-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="76921-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76921-111">EXAMPLES</span></span>

### <span data-ttu-id="76921-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76921-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="76921-113">Questo comando imposta i criteri di conservazione a breve termine per il database01 su 35 giorni.</span><span class="sxs-lookup"><span data-stu-id="76921-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="76921-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="76921-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="76921-115">Questo comando imposta i criteri di conservazione a breve termine per il database01 su 35 giorni tramite piping in un oggetto di database.</span><span class="sxs-lookup"><span data-stu-id="76921-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="76921-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="76921-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="76921-117">Questo comando imposta i criteri di conservazione a breve termine per tutti i database eliminati denominati DB1 tramite piping in un oggetto di database eliminato.</span><span class="sxs-lookup"><span data-stu-id="76921-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="76921-118">Tenere presente che è possibile ridurre il periodo di conservazione solo per i database eliminati.</span><span class="sxs-lookup"><span data-stu-id="76921-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="76921-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76921-119">PARAMETERS</span></span>

### <span data-ttu-id="76921-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76921-120">-DatabaseName</span></span>
<span data-ttu-id="76921-121">Nome del database delle istanze SQL Azure per cui recuperare i backup.</span><span class="sxs-lookup"><span data-stu-id="76921-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76921-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76921-122">-DefaultProfile</span></span>
<span data-ttu-id="76921-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76921-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76921-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="76921-124">-DeletionDate</span></span>
<span data-ttu-id="76921-125">Data di eliminazione del database delle istanze di Azure SQL per cui recuperare i backup con precisione in millisecondi (ad esempio 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="76921-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76921-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76921-126">-InputObject</span></span>
<span data-ttu-id="76921-127">Oggetto di database live o eliminato per cui ottenere/impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="76921-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76921-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="76921-128">-InstanceName</span></span>
<span data-ttu-id="76921-129">Il nome dell'istanza SQL gestita di Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="76921-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76921-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76921-130">-ResourceGroupName</span></span>
<span data-ttu-id="76921-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76921-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76921-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76921-132">-ResourceId</span></span>
<span data-ttu-id="76921-133">ID risorsa per i criteri di conservazione a breve termine.</span><span class="sxs-lookup"><span data-stu-id="76921-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76921-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="76921-134">-RetentionDays</span></span>
<span data-ttu-id="76921-135">Giorni di conservazione del backup.</span><span class="sxs-lookup"><span data-stu-id="76921-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="76921-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76921-136">-Confirm</span></span>
<span data-ttu-id="76921-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76921-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76921-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76921-138">-WhatIf</span></span>
<span data-ttu-id="76921-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76921-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76921-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76921-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76921-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76921-141">CommonParameters</span></span>
<span data-ttu-id="76921-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76921-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76921-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76921-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76921-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="76921-144">INPUTS</span></span>

### <span data-ttu-id="76921-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="76921-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="76921-146">System.String</span><span class="sxs-lookup"><span data-stu-id="76921-146">System.String</span></span>

## <span data-ttu-id="76921-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76921-147">OUTPUTS</span></span>

### <span data-ttu-id="76921-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="76921-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="76921-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="76921-149">NOTES</span></span>

## <span data-ttu-id="76921-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76921-150">RELATED LINKS</span></span>
