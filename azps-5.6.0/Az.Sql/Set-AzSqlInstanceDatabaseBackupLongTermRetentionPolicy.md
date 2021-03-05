---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b8284d4f2ac5b28baffed630e789fc002c2c7d9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015853"
---
# <span data-ttu-id="0246b-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0246b-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="0246b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0246b-102">SYNOPSIS</span></span>
<span data-ttu-id="0246b-103">Il cmdlet **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** imposta i criteri di conservazione a lungo termine di un database gestito.</span><span class="sxs-lookup"><span data-stu-id="0246b-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="0246b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0246b-104">SYNTAX</span></span>

### <span data-ttu-id="0246b-105">WeeklyRetentionRequired (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0246b-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0246b-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="0246b-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0246b-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="0246b-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0246b-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="0246b-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0246b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0246b-109">DESCRIPTION</span></span>
<span data-ttu-id="0246b-110">Il cmdlet **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** imposta i criteri di conservazione a lungo termine per questo database gestito.</span><span class="sxs-lookup"><span data-stu-id="0246b-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="0246b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0246b-111">EXAMPLES</span></span>

### <span data-ttu-id="0246b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0246b-112">Example 1</span></span>
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

<span data-ttu-id="0246b-113">Configura i criteri settimanali di conservazione a lungo termine del database su una settimana.</span><span class="sxs-lookup"><span data-stu-id="0246b-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="0246b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0246b-114">Example 2</span></span>
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

<span data-ttu-id="0246b-115">Questo comando rimuove i criteri di conservazione a lungo termine dal database.</span><span class="sxs-lookup"><span data-stu-id="0246b-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="0246b-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0246b-116">Example 3</span></span>

<span data-ttu-id="0246b-117">Il Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet imposta i criteri di conservazione a lungo termine di un database gestito.</span><span class="sxs-lookup"><span data-stu-id="0246b-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="0246b-118">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="0246b-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="0246b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0246b-119">PARAMETERS</span></span>

### <span data-ttu-id="0246b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0246b-120">-DatabaseName</span></span>
<span data-ttu-id="0246b-121">Nome del database gestito di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="0246b-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="0246b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0246b-122">-DefaultProfile</span></span>
<span data-ttu-id="0246b-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0246b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0246b-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0246b-124">-InstanceName</span></span>
<span data-ttu-id="0246b-125">Nome dell'istanza gestita di Azure a cui appartiene il database.</span><span class="sxs-lookup"><span data-stu-id="0246b-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="0246b-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="0246b-126">-MonthlyRetention</span></span>
<span data-ttu-id="0246b-127">Conservazione mensile.</span><span class="sxs-lookup"><span data-stu-id="0246b-127">The Monthly Retention.</span></span>
<span data-ttu-id="0246b-128">Se invece di una stringa ISO 8601 viene passato solo un numero, come unità verranno presunti i giorni.</span><span class="sxs-lookup"><span data-stu-id="0246b-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="0246b-129">Ci sono un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="0246b-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="0246b-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="0246b-130">-RemovePolicy</span></span>
<span data-ttu-id="0246b-131">Se specificato, i criteri per il database verranno cancellati.</span><span class="sxs-lookup"><span data-stu-id="0246b-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="0246b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0246b-132">-ResourceGroupName</span></span>
<span data-ttu-id="0246b-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0246b-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="0246b-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="0246b-134">-WeeklyRetention</span></span>
<span data-ttu-id="0246b-135">Conservazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="0246b-135">The Weekly Retention.</span></span>
<span data-ttu-id="0246b-136">Se invece di una stringa ISO 8601 viene passato solo un numero, come unità verranno presunti i giorni.</span><span class="sxs-lookup"><span data-stu-id="0246b-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="0246b-137">Ci sono un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="0246b-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="0246b-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="0246b-138">-WeekOfYear</span></span>
<span data-ttu-id="0246b-139">Settimana dell'anno, da 1 a 52, da salvare per la conservazione annuale.</span><span class="sxs-lookup"><span data-stu-id="0246b-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="0246b-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="0246b-140">-YearlyRetention</span></span>
<span data-ttu-id="0246b-141">Conservazione annuale.</span><span class="sxs-lookup"><span data-stu-id="0246b-141">The Yearly Retention.</span></span>
<span data-ttu-id="0246b-142">Se invece di una stringa ISO 8601 viene passato solo un numero, come unità verranno presunti i giorni.</span><span class="sxs-lookup"><span data-stu-id="0246b-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="0246b-143">Ci sono un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="0246b-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="0246b-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0246b-144">-Confirm</span></span>
<span data-ttu-id="0246b-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0246b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0246b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0246b-146">-WhatIf</span></span>
<span data-ttu-id="0246b-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0246b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0246b-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0246b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0246b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0246b-149">CommonParameters</span></span>
<span data-ttu-id="0246b-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0246b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0246b-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0246b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0246b-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="0246b-152">INPUTS</span></span>

### <span data-ttu-id="0246b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0246b-153">System.String</span></span>

### <span data-ttu-id="0246b-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0246b-154">System.Int32</span></span>

## <span data-ttu-id="0246b-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0246b-155">OUTPUTS</span></span>

### <span data-ttu-id="0246b-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0246b-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="0246b-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="0246b-157">NOTES</span></span>

## <span data-ttu-id="0246b-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0246b-158">RELATED LINKS</span></span>

[<span data-ttu-id="0246b-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0246b-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="0246b-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0246b-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="0246b-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0246b-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="0246b-162">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="0246b-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)