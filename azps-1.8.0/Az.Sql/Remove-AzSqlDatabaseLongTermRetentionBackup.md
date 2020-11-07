---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 8fd76e227951afefcbb8f7b04cf4ae3616ef5ef7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676816"
---
# <span data-ttu-id="1ee3f-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1ee3f-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="1ee3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ee3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee3f-103">Elimina un backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="1ee3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ee3f-104">SYNTAX</span></span>

### <span data-ttu-id="1ee3f-105">RemoveBackupDefault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ee3f-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ee3f-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ee3f-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ee3f-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ee3f-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee3f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ee3f-108">DESCRIPTION</span></span>
<span data-ttu-id="1ee3f-109">Il cmdlet **Remove-AzSqlDatabaseLongTermRetentionBackup** Elimina il backup specificato.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="1ee3f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ee3f-110">EXAMPLES</span></span>

### <span data-ttu-id="1ee3f-111">Esempio 1: eliminare un singolo backup</span><span class="sxs-lookup"><span data-stu-id="1ee3f-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="1ee3f-112">Elimina il backup con il nome 601061b7-D10B-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="1ee3f-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="1ee3f-113">Esempio 2: eliminare tutti i backup per una posizione</span><span class="sxs-lookup"><span data-stu-id="1ee3f-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="1ee3f-114">Questo comando Elimina tutti i backup di conservazione a lungo termine per la posizione northeurope.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="1ee3f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ee3f-115">PARAMETERS</span></span>

### <span data-ttu-id="1ee3f-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="1ee3f-116">-BackupName</span></span>
<span data-ttu-id="1ee3f-117">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-117">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ee3f-118">-DatabaseName</span></span>
<span data-ttu-id="1ee3f-119">Nome del database SQL di Azure a cui è associato il backup.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee3f-120">-DefaultProfile</span></span>
<span data-ttu-id="1ee3f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ee3f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1ee3f-122">-Force</span></span>
<span data-ttu-id="1ee3f-123">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="1ee3f-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ee3f-124">-InputObject</span></span>
<span data-ttu-id="1ee3f-125">Oggetto di backup di conservazione a lungo termine del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1ee3f-126">-Location</span></span>
<span data-ttu-id="1ee3f-127">Posizione del server di origine del backup.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-127">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ee3f-128">-ResourceId</span></span>
<span data-ttu-id="1ee3f-129">ID risorsa del backup del database di conservazione a lungo termine da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1ee3f-130">-ServerName</span></span>
<span data-ttu-id="1ee3f-131">Nome di Azure SQL Server in cui è presente il backup.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ee3f-132">-Confirm</span></span>
<span data-ttu-id="1ee3f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee3f-134">-WhatIf</span></span>
<span data-ttu-id="1ee3f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee3f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee3f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee3f-137">CommonParameters</span></span>
<span data-ttu-id="1ee3f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee3f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee3f-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ee3f-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee3f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ee3f-140">INPUTS</span></span>

### <span data-ttu-id="1ee3f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee3f-141">System.String</span></span>

## <span data-ttu-id="1ee3f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ee3f-142">OUTPUTS</span></span>

### <span data-ttu-id="1ee3f-143">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="1ee3f-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="1ee3f-144">Note</span><span class="sxs-lookup"><span data-stu-id="1ee3f-144">NOTES</span></span>

## <span data-ttu-id="1ee3f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ee3f-145">RELATED LINKS</span></span>

[<span data-ttu-id="1ee3f-146">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1ee3f-146">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1ee3f-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ee3f-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1ee3f-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ee3f-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1ee3f-149">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1ee3f-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)