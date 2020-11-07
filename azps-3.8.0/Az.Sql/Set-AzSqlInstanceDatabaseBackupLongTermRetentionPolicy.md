---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864980"
---
# <span data-ttu-id="3a64f-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a64f-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="3a64f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a64f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a64f-103">Il cmdlet **set-AzSqlInstanceDatabaseLongTermRetentionBackup** imposta i criteri di conservazione a lungo termine di un database gestito.</span><span class="sxs-lookup"><span data-stu-id="3a64f-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="3a64f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a64f-104">SYNTAX</span></span>

### <span data-ttu-id="3a64f-105">WeeklyRetentionRequired (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a64f-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a64f-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="3a64f-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a64f-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="3a64f-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a64f-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="3a64f-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a64f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a64f-109">DESCRIPTION</span></span>
<span data-ttu-id="3a64f-110">Il cmdlet **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** imposta i criteri di conservazione a lungo termine per il database gestito.</span><span class="sxs-lookup"><span data-stu-id="3a64f-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="3a64f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a64f-111">EXAMPLES</span></span>

### <span data-ttu-id="3a64f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a64f-112">Example 1</span></span>
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

<span data-ttu-id="3a64f-113">Configura i criteri settimanali di conservazione a lungo termine del database in una settimana.</span><span class="sxs-lookup"><span data-stu-id="3a64f-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="3a64f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3a64f-114">Example 2</span></span>
```
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


<span data-ttu-id="3a64f-115">Questo comando rimuove i criteri di conservazione a lungo termine dal database.</span><span class="sxs-lookup"><span data-stu-id="3a64f-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="3a64f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a64f-116">PARAMETERS</span></span>

### <span data-ttu-id="3a64f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a64f-117">-DatabaseName</span></span>
<span data-ttu-id="3a64f-118">Nome del database gestito di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="3a64f-118">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="3a64f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a64f-119">-DefaultProfile</span></span>
<span data-ttu-id="3a64f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a64f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3a64f-121">-InstanceName</span></span>
<span data-ttu-id="3a64f-122">Nome dell'istanza di Azure Managed a cui appartiene il database.</span><span class="sxs-lookup"><span data-stu-id="3a64f-122">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="3a64f-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="3a64f-123">-MonthlyRetention</span></span>
<span data-ttu-id="3a64f-124">Conservazione mensile.</span><span class="sxs-lookup"><span data-stu-id="3a64f-124">The Monthly Retention.</span></span>
<span data-ttu-id="3a64f-125">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="3a64f-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="3a64f-126">È previsto un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="3a64f-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="3a64f-127">-RemovePolicy</span></span>
<span data-ttu-id="3a64f-128">Se specificato, i criteri per il database verranno deselezionati.</span><span class="sxs-lookup"><span data-stu-id="3a64f-128">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="3a64f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a64f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3a64f-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a64f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a64f-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="3a64f-131">-WeeklyRetention</span></span>
<span data-ttu-id="3a64f-132">Ritenzione settimanale.</span><span class="sxs-lookup"><span data-stu-id="3a64f-132">The Weekly Retention.</span></span>
<span data-ttu-id="3a64f-133">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="3a64f-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="3a64f-134">È previsto un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="3a64f-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="3a64f-135">-WeekOfYear</span></span>
<span data-ttu-id="3a64f-136">La settimana dell'anno, da 1 a 52, per salvare la conservazione annua.</span><span class="sxs-lookup"><span data-stu-id="3a64f-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="3a64f-137">-YearlyRetention</span></span>
<span data-ttu-id="3a64f-138">Ritenzione annua.</span><span class="sxs-lookup"><span data-stu-id="3a64f-138">The Yearly Retention.</span></span>
<span data-ttu-id="3a64f-139">Se viene passato solo un numero anziché una stringa ISO 8601, i giorni verranno assunti come unità.</span><span class="sxs-lookup"><span data-stu-id="3a64f-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="3a64f-140">È previsto un minimo di 7 giorni e un massimo di 10 anni.</span><span class="sxs-lookup"><span data-stu-id="3a64f-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a64f-141">-Confirm</span></span>
<span data-ttu-id="3a64f-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a64f-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a64f-143">-WhatIf</span></span>
<span data-ttu-id="3a64f-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a64f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a64f-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a64f-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a64f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a64f-146">CommonParameters</span></span>
<span data-ttu-id="3a64f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a64f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a64f-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a64f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a64f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a64f-149">INPUTS</span></span>

### <span data-ttu-id="3a64f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3a64f-150">System.String</span></span>

### <span data-ttu-id="3a64f-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3a64f-151">System.Int32</span></span>

## <span data-ttu-id="3a64f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a64f-152">OUTPUTS</span></span>

### <span data-ttu-id="3a64f-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3a64f-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3a64f-154">Note</span><span class="sxs-lookup"><span data-stu-id="3a64f-154">NOTES</span></span>

## <span data-ttu-id="3a64f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a64f-155">RELATED LINKS</span></span>

[<span data-ttu-id="3a64f-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a64f-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3a64f-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3a64f-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3a64f-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3a64f-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3a64f-159">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="3a64f-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)