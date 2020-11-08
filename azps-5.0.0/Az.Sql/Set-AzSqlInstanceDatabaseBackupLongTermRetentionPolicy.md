---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193140"
---
# <span data-ttu-id="dfbf6-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfbf6-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="dfbf6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbf6-103">Il cmdlet **set-AzSqlInstanceDatabaseLongTermRetentionBackup** imposta i criteri di conservazione a lungo termine di un database gestito.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="dfbf6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfbf6-104">SYNTAX</span></span>

### <span data-ttu-id="dfbf6-105">WeeklyRetentionRequired (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfbf6-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbf6-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="dfbf6-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbf6-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="dfbf6-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfbf6-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="dfbf6-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfbf6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfbf6-109">DESCRIPTION</span></span>
<span data-ttu-id="dfbf6-110">Il cmdlet **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** imposta i criteri di conservazione a lungo termine per il database gestito.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="dfbf6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfbf6-111">EXAMPLES</span></span>

### <span data-ttu-id="dfbf6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfbf6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="dfbf6-113">Configura i criteri settimanali di conservazione a lungo termine del database in una settimana.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="dfbf6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dfbf6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="dfbf6-115">Questo comando rimuove i criteri di conservazione a lungo termine dal database.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="dfbf6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dfbf6-116">Example 3</span></span>

<span data-ttu-id="dfbf6-117">Il cmdlet Set-AzSqlInstanceDatabaseLongTermRetentionBackup imposta i criteri di conservazione a lungo termine di un database gestito.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="dfbf6-118">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="dfbf6-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="dfbf6-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfbf6-119">PARAMETERS</span></span>

### <span data-ttu-id="dfbf6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dfbf6-120">-DatabaseName</span></span>
<span data-ttu-id="dfbf6-121">Nome del database gestito di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="dfbf6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbf6-122">-DefaultProfile</span></span>
<span data-ttu-id="dfbf6-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfbf6-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="dfbf6-124">-InstanceName</span></span>
<span data-ttu-id="dfbf6-125">Nome dell'istanza di Azure Managed a cui appartiene il database.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="dfbf6-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="dfbf6-126">-MonthlyRetention</span></span>
<span data-ttu-id="dfbf6-127">Conservazione mensile.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-127">The Monthly Retention.</span></span>
<span data-ttu-id="dfbf6-128">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dfbf6-129">È previsto un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="dfbf6-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="dfbf6-130">-RemovePolicy</span></span>
<span data-ttu-id="dfbf6-131">Se specificato, i criteri per il database verranno deselezionati.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="dfbf6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbf6-132">-ResourceGroupName</span></span>
<span data-ttu-id="dfbf6-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfbf6-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="dfbf6-134">-WeeklyRetention</span></span>
<span data-ttu-id="dfbf6-135">Ritenzione settimanale.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-135">The Weekly Retention.</span></span>
<span data-ttu-id="dfbf6-136">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dfbf6-137">È previsto un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="dfbf6-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="dfbf6-138">-WeekOfYear</span></span>
<span data-ttu-id="dfbf6-139">La settimana dell'anno, da 1 a 52, per salvare la conservazione annua.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="dfbf6-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="dfbf6-140">-YearlyRetention</span></span>
<span data-ttu-id="dfbf6-141">Ritenzione annua.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-141">The Yearly Retention.</span></span>
<span data-ttu-id="dfbf6-142">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dfbf6-143">È previsto un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="dfbf6-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfbf6-144">-Confirm</span></span>
<span data-ttu-id="dfbf6-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbf6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbf6-146">-WhatIf</span></span>
<span data-ttu-id="dfbf6-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfbf6-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbf6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbf6-149">CommonParameters</span></span>
<span data-ttu-id="dfbf6-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbf6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbf6-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfbf6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbf6-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfbf6-152">INPUTS</span></span>

### <span data-ttu-id="dfbf6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="dfbf6-153">System.String</span></span>

### <span data-ttu-id="dfbf6-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dfbf6-154">System.Int32</span></span>

## <span data-ttu-id="dfbf6-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfbf6-155">OUTPUTS</span></span>

### <span data-ttu-id="dfbf6-156">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="dfbf6-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="dfbf6-157">Note</span><span class="sxs-lookup"><span data-stu-id="dfbf6-157">NOTES</span></span>

## <span data-ttu-id="dfbf6-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfbf6-158">RELATED LINKS</span></span>

[<span data-ttu-id="dfbf6-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfbf6-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="dfbf6-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dfbf6-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dfbf6-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dfbf6-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dfbf6-162">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="dfbf6-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)