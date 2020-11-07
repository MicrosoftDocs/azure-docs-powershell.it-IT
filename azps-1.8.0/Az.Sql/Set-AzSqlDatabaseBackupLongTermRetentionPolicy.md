---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c11d8de5f7cd60bd71f759feeceaf043c4fd869b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676758"
---
# <span data-ttu-id="271cf-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="271cf-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="271cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="271cf-102">SYNOPSIS</span></span>
<span data-ttu-id="271cf-103">Imposta i criteri di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="271cf-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="271cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="271cf-104">SYNTAX</span></span>

### <span data-ttu-id="271cf-105">WeeklyRetentionRequired (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="271cf-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271cf-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="271cf-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="271cf-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="271cf-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271cf-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="271cf-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="271cf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="271cf-109">DESCRIPTION</span></span>
<span data-ttu-id="271cf-110">Il cmdlet **set-AzSqlDatabaseBackupLongTermRetentionPolicy** imposta i criteri di conservazione a lungo termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="271cf-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="271cf-111">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="271cf-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="271cf-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="271cf-112">EXAMPLES</span></span>

### <span data-ttu-id="271cf-113">Esempio 1: impostare la conservazione settimanale per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="271cf-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="271cf-114">Questo imposta i criteri di conservazione a lungo termine di Database01 per salvare ogni backup completo settimanale per 2 settimane</span><span class="sxs-lookup"><span data-stu-id="271cf-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="271cf-115">Esempio 2: impostare la conservazione mensile per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="271cf-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="271cf-116">Questo imposta i criteri di conservazione a lungo termine di Database01 per salvare il primo backup completo di ogni mese per 5 anni</span><span class="sxs-lookup"><span data-stu-id="271cf-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="271cf-117">Esempio 3: impostare la conservazione annuale per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="271cf-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="271cf-118">Questo imposta i criteri di conservazione a lungo termine di Database01 per salvare il backup completo adottato la 26a settimana dell'anno per 10 anni</span><span class="sxs-lookup"><span data-stu-id="271cf-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="271cf-119">Esempio 4: impostare ogni conservazione per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="271cf-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="271cf-120">In questo articolo vengono imposti i criteri di conservazione a lungo termine di Database01 per salvare ogni backup completo per 14 giorni, il primo backup completo di ogni mese per 24 settimane e il backup completo adottato la 26a settimana dell'anno per 10 anni</span><span class="sxs-lookup"><span data-stu-id="271cf-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="271cf-121">Esempio 4: rimuovere i criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="271cf-121">Example 4: Remove the long term retention policy</span></span>
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

<span data-ttu-id="271cf-122">Rimuove il criterio per Database01 in modo che non salvi più i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="271cf-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="271cf-123">Ciò non influirà sui backup già eseguiti</span><span class="sxs-lookup"><span data-stu-id="271cf-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="271cf-124">Esempio 4: rimuovere i criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="271cf-124">Example 4: Remove the long term retention policy</span></span>
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

<span data-ttu-id="271cf-125">Questo è un altro modo per rimuovere i criteri per Database01 in modo che non salvi più i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="271cf-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="271cf-126">Ciò non influirà sui backup già eseguiti</span><span class="sxs-lookup"><span data-stu-id="271cf-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="271cf-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="271cf-127">PARAMETERS</span></span>

### <span data-ttu-id="271cf-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="271cf-128">-DatabaseName</span></span>
<span data-ttu-id="271cf-129">Nome del database SQL di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="271cf-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="271cf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271cf-130">-DefaultProfile</span></span>
<span data-ttu-id="271cf-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="271cf-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="271cf-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="271cf-132">-MonthlyRetention</span></span>
<span data-ttu-id="271cf-133">Conservazione mensile.</span><span class="sxs-lookup"><span data-stu-id="271cf-133">The Monthly Retention.</span></span>
<span data-ttu-id="271cf-134">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="271cf-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="271cf-135">C'è un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="271cf-135">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="271cf-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="271cf-136">-RemovePolicy</span></span>
<span data-ttu-id="271cf-137">Se specificato, il criterio per il database verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="271cf-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="271cf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271cf-138">-ResourceGroupName</span></span>
<span data-ttu-id="271cf-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="271cf-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="271cf-140">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="271cf-140">-ServerName</span></span>
<span data-ttu-id="271cf-141">Il nome di Azure SQL Server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="271cf-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="271cf-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="271cf-142">-WeeklyRetention</span></span>
<span data-ttu-id="271cf-143">Ritenzione settimanale.</span><span class="sxs-lookup"><span data-stu-id="271cf-143">The Weekly Retention.</span></span>
<span data-ttu-id="271cf-144">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="271cf-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="271cf-145">C'è un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="271cf-145">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="271cf-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="271cf-146">-WeekOfYear</span></span>
<span data-ttu-id="271cf-147">La settimana dell'anno, da 1 a 52, per salvare la conservazione annua.</span><span class="sxs-lookup"><span data-stu-id="271cf-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="271cf-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="271cf-148">-YearlyRetention</span></span>
<span data-ttu-id="271cf-149">Ritenzione annua.</span><span class="sxs-lookup"><span data-stu-id="271cf-149">The Yearly Retention.</span></span>
<span data-ttu-id="271cf-150">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="271cf-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="271cf-151">C'è un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="271cf-151">There is a minumum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="271cf-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="271cf-152">-Confirm</span></span>
<span data-ttu-id="271cf-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="271cf-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="271cf-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="271cf-154">-WhatIf</span></span>
<span data-ttu-id="271cf-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="271cf-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="271cf-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="271cf-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="271cf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271cf-157">CommonParameters</span></span>
<span data-ttu-id="271cf-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271cf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271cf-159">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="271cf-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271cf-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="271cf-160">INPUTS</span></span>

### <span data-ttu-id="271cf-161">System. String</span><span class="sxs-lookup"><span data-stu-id="271cf-161">System.String</span></span>

### <span data-ttu-id="271cf-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="271cf-162">System.Int32</span></span>

## <span data-ttu-id="271cf-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="271cf-163">OUTPUTS</span></span>

### <span data-ttu-id="271cf-164">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="271cf-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="271cf-165">Note</span><span class="sxs-lookup"><span data-stu-id="271cf-165">NOTES</span></span>

## <span data-ttu-id="271cf-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="271cf-166">RELATED LINKS</span></span>

[<span data-ttu-id="271cf-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="271cf-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="271cf-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="271cf-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="271cf-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="271cf-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="271cf-170">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="271cf-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)