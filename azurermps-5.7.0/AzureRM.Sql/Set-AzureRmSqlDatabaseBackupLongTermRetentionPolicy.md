---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c5450ea3ffdcc8c76fa88c8721902b8f8ae77794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512167"
---
# <span data-ttu-id="6b74c-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b74c-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="6b74c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b74c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b74c-103">Imposta i criteri di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="6b74c-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b74c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b74c-104">SYNTAX</span></span>

### <span data-ttu-id="6b74c-105">WeeklyRetentionRequired (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b74c-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b74c-106">Legacy</span><span class="sxs-lookup"><span data-stu-id="6b74c-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b74c-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="6b74c-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b74c-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="6b74c-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>] [-MonthlyRetention] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b74c-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="6b74c-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>]
 [[-MonthlyRetention] <String>] [-YearlyRetention] <String> [-WeekOfYear] <Int32> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b74c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b74c-110">DESCRIPTION</span></span>
<span data-ttu-id="6b74c-111">Il cmdlet **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** imposta i criteri di conservazione a lungo termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="6b74c-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="6b74c-112">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="6b74c-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="6b74c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b74c-113">EXAMPLES</span></span>

### <span data-ttu-id="6b74c-114">Esempio 1: impostare la conservazione settimanale per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="6b74c-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6b74c-115">Questo imposta i criteri di conservazione a lungo termine di Database01 per salvare ogni backup completo settimanale per 2 settimane</span><span class="sxs-lookup"><span data-stu-id="6b74c-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="6b74c-116">Esempio 2: impostare la conservazione mensile per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="6b74c-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6b74c-117">Questo imposta i criteri di conservazione a lungo termine di Database01 per salvare il primo backup completo di ogni mese per 5 anni</span><span class="sxs-lookup"><span data-stu-id="6b74c-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="6b74c-118">Esempio 3: impostare la conservazione annuale per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="6b74c-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6b74c-119">Questo imposta i criteri di conservazione a lungo termine di Database01 per salvare il backup completo adottato la 26a settimana dell'anno per 10 anni</span><span class="sxs-lookup"><span data-stu-id="6b74c-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="6b74c-120">Esempio 4: impostare ogni conservazione per la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="6b74c-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6b74c-121">In questo articolo vengono imposti i criteri di conservazione a lungo termine di Database01 per salvare ogni backup completo per 14 giorni, il primo backup completo di ogni mese per 24 settimane e il backup completo adottato la 26a settimana dell'anno per 10 anni</span><span class="sxs-lookup"><span data-stu-id="6b74c-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="6b74c-122">Esempio 4: rimuovere i criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="6b74c-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6b74c-123">Rimuove il criterio per Database01 in modo che non salvi più i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="6b74c-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="6b74c-124">Ciò non influirà sui backup già eseguiti</span><span class="sxs-lookup"><span data-stu-id="6b74c-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="6b74c-125">Esempio 4: rimuovere i criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="6b74c-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6b74c-126">Questo è un altro modo per rimuovere i criteri per Database01 in modo che non salvi più i backup di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="6b74c-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="6b74c-127">Ciò non influirà sui backup già eseguiti</span><span class="sxs-lookup"><span data-stu-id="6b74c-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="6b74c-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b74c-128">PARAMETERS</span></span>

### <span data-ttu-id="6b74c-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b74c-129">-DatabaseName</span></span>
<span data-ttu-id="6b74c-130">Nome del database SQL di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="6b74c-130">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b74c-131">-DefaultProfile</span></span>
<span data-ttu-id="6b74c-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b74c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="6b74c-133">-MonthlyRetention</span></span>
<span data-ttu-id="6b74c-134">Conservazione mensile.</span><span class="sxs-lookup"><span data-stu-id="6b74c-134">The Monthly Retention.</span></span>
<span data-ttu-id="6b74c-135">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="6b74c-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="6b74c-136">C'è un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="6b74c-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="6b74c-137">-RemovePolicy</span></span>
<span data-ttu-id="6b74c-138">Se specificato, il criterio per il database verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b74c-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b74c-139">-ResourceGroupName</span></span>
<span data-ttu-id="6b74c-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b74c-140">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b74c-141">-ResourceId</span></span>
<span data-ttu-id="6b74c-142">ID risorsa dei criteri di conservazione a lungo termine di backup.</span><span class="sxs-lookup"><span data-stu-id="6b74c-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-143">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6b74c-143">-ServerName</span></span>
<span data-ttu-id="6b74c-144">Il nome di Azure SQL Server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="6b74c-144">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-145">-Stato</span><span class="sxs-lookup"><span data-stu-id="6b74c-145">-State</span></span>
<span data-ttu-id="6b74c-146">Stato dei criteri di backup a lungo termine, "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="6b74c-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="6b74c-147">-WeeklyRetention</span></span>
<span data-ttu-id="6b74c-148">Ritenzione settimanale.</span><span class="sxs-lookup"><span data-stu-id="6b74c-148">The Weekly Retention.</span></span>
<span data-ttu-id="6b74c-149">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="6b74c-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="6b74c-150">C'è un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="6b74c-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="6b74c-151">-WeekOfYear</span></span>
<span data-ttu-id="6b74c-152">La settimana dell'anno, da 1 a 52, per salvare la conservazione annua.</span><span class="sxs-lookup"><span data-stu-id="6b74c-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="6b74c-153">-YearlyRetention</span></span>
<span data-ttu-id="6b74c-154">Ritenzione annua.</span><span class="sxs-lookup"><span data-stu-id="6b74c-154">The Yearly Retention.</span></span>
<span data-ttu-id="6b74c-155">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="6b74c-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="6b74c-156">C'è un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="6b74c-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b74c-157">-Confirm</span></span>
<span data-ttu-id="6b74c-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b74c-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b74c-159">-WhatIf</span></span>
<span data-ttu-id="6b74c-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b74c-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b74c-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b74c-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b74c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b74c-162">CommonParameters</span></span>
<span data-ttu-id="6b74c-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b74c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6b74c-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b74c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b74c-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b74c-165">INPUTS</span></span>

### <span data-ttu-id="6b74c-166">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6b74c-166">None</span></span>
<span data-ttu-id="6b74c-167">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6b74c-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b74c-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b74c-168">OUTPUTS</span></span>

### <span data-ttu-id="6b74c-169">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6b74c-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="6b74c-170">Note</span><span class="sxs-lookup"><span data-stu-id="6b74c-170">NOTES</span></span>

## <span data-ttu-id="6b74c-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b74c-171">RELATED LINKS</span></span>

[<span data-ttu-id="6b74c-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b74c-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6b74c-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6b74c-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6b74c-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6b74c-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6b74c-175">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="6b74c-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
