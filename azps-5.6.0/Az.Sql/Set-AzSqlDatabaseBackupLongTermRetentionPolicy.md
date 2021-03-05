---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 9726d945b4e0fada340d06e780008f1921fb6f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995005"
---
# <span data-ttu-id="a00e1-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a00e1-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="a00e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a00e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a00e1-103">Imposta i criteri di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="a00e1-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="a00e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a00e1-104">SYNTAX</span></span>

### <span data-ttu-id="a00e1-105">WeeklyRetentionRequired (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a00e1-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a00e1-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="a00e1-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a00e1-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="a00e1-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a00e1-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="a00e1-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a00e1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a00e1-109">DESCRIPTION</span></span>
<span data-ttu-id="a00e1-110">Il cmdlet **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** imposta il criterio di conservazione a lungo termine registrato su questo database.</span><span class="sxs-lookup"><span data-stu-id="a00e1-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="a00e1-111">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="a00e1-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="a00e1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a00e1-112">EXAMPLES</span></span>

### <span data-ttu-id="a00e1-113">Esempio 1: Impostare la conservazione settimanale per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="a00e1-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="a00e1-114">Imposta i criteri di conservazione a lungo termine di database01 in modo da salvare ogni backup completo settimanale per 2 settimane</span><span class="sxs-lookup"><span data-stu-id="a00e1-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="a00e1-115">Esempio 2: Impostare la conservazione mensile per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="a00e1-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="a00e1-116">Imposta i criteri di conservazione a lungo termine di database01 in modo da salvare il primo backup completo di ogni mese per 5 anni</span><span class="sxs-lookup"><span data-stu-id="a00e1-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="a00e1-117">Esempio 3: Impostare la conservazione annuale per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="a00e1-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="a00e1-118">Imposta i criteri di conservazione a lungo termine di database01 in modo da salvare il backup completo eseguito nella 26a settimana dell'anno per 10 anni</span><span class="sxs-lookup"><span data-stu-id="a00e1-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="a00e1-119">Esempio 4: Impostare ogni conservazione per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="a00e1-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="a00e1-120">Imposta i criteri di conservazione a lungo termine di database01 in modo da salvare ogni backup completo per 14 giorni, il primo backup completo di ogni mese per 24 settimane e il backup completo eseguito nella 26a settimana dell'anno per 10 anni</span><span class="sxs-lookup"><span data-stu-id="a00e1-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="a00e1-121">Esempio 5: Rimuovere i criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="a00e1-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="a00e1-122">Rimuove i criteri per database01 in modo che non salvi più i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="a00e1-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="a00e1-123">Questa operazione non influisce sui backup già evasi</span><span class="sxs-lookup"><span data-stu-id="a00e1-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="a00e1-124">Esempio 6: Rimuovere i criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="a00e1-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="a00e1-125">Si tratta di un altro modo per rimuovere i criteri per database01, quindi non salva più i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="a00e1-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="a00e1-126">Questa operazione non influisce sui backup già evasi</span><span class="sxs-lookup"><span data-stu-id="a00e1-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="a00e1-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a00e1-127">PARAMETERS</span></span>

### <span data-ttu-id="a00e1-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a00e1-128">-DatabaseName</span></span>
<span data-ttu-id="a00e1-129">Il nome del database SQL Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="a00e1-129">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00e1-130">-DefaultProfile</span></span>
<span data-ttu-id="a00e1-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a00e1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a00e1-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="a00e1-132">-MonthlyRetention</span></span>
<span data-ttu-id="a00e1-133">Conservazione mensile.</span><span class="sxs-lookup"><span data-stu-id="a00e1-133">The Monthly Retention.</span></span>
<span data-ttu-id="a00e1-134">Se invece di una stringa ISO 8601 viene passato solo un numero, come unità verranno presunti i giorni.</span><span class="sxs-lookup"><span data-stu-id="a00e1-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="a00e1-135">Ci sono un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="a00e1-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="a00e1-136">-RemovePolicy</span></span>
<span data-ttu-id="a00e1-137">Se specificato, i criteri per il database verranno rimossi.</span><span class="sxs-lookup"><span data-stu-id="a00e1-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00e1-138">-ResourceGroupName</span></span>
<span data-ttu-id="a00e1-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a00e1-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a00e1-140">-ServerName</span></span>
<span data-ttu-id="a00e1-141">Nome della cartella di SQL Server Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="a00e1-141">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="a00e1-142">-WeeklyRetention</span></span>
<span data-ttu-id="a00e1-143">Conservazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="a00e1-143">The Weekly Retention.</span></span>
<span data-ttu-id="a00e1-144">Se invece di una stringa ISO 8601 viene passato solo un numero, come unità verranno presunti i giorni.</span><span class="sxs-lookup"><span data-stu-id="a00e1-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="a00e1-145">Ci sono un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="a00e1-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="a00e1-146">-WeekOfYear</span></span>
<span data-ttu-id="a00e1-147">Settimana dell'anno, da 1 a 52, da salvare per la conservazione annuale.</span><span class="sxs-lookup"><span data-stu-id="a00e1-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="a00e1-148">-YearlyRetention</span></span>
<span data-ttu-id="a00e1-149">Conservazione annuale.</span><span class="sxs-lookup"><span data-stu-id="a00e1-149">The Yearly Retention.</span></span>
<span data-ttu-id="a00e1-150">Se invece di una stringa ISO 8601 viene passato solo un numero, come unità verranno presunti i giorni.</span><span class="sxs-lookup"><span data-stu-id="a00e1-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="a00e1-151">Ci sono un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="a00e1-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00e1-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a00e1-152">-Confirm</span></span>
<span data-ttu-id="a00e1-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a00e1-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a00e1-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00e1-154">-WhatIf</span></span>
<span data-ttu-id="a00e1-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a00e1-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a00e1-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a00e1-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a00e1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00e1-157">CommonParameters</span></span>
<span data-ttu-id="a00e1-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00e1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00e1-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a00e1-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00e1-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="a00e1-160">INPUTS</span></span>

### <span data-ttu-id="a00e1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a00e1-161">System.String</span></span>

### <span data-ttu-id="a00e1-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a00e1-162">System.Int32</span></span>

## <span data-ttu-id="a00e1-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a00e1-163">OUTPUTS</span></span>

### <span data-ttu-id="a00e1-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a00e1-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="a00e1-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="a00e1-165">NOTES</span></span>

## <span data-ttu-id="a00e1-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a00e1-166">RELATED LINKS</span></span>

[<span data-ttu-id="a00e1-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a00e1-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="a00e1-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a00e1-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a00e1-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a00e1-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a00e1-170">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="a00e1-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)