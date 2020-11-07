---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686352"
---
# <span data-ttu-id="c57e8-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c57e8-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="c57e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c57e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c57e8-103">Ottiene un database di criteri di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="c57e8-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c57e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c57e8-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c57e8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c57e8-105">DESCRIPTION</span></span>
<span data-ttu-id="c57e8-106">Il cmdlet **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** ottiene i criteri di conservazione a lungo termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="c57e8-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="c57e8-107">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="c57e8-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="c57e8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c57e8-108">EXAMPLES</span></span>

### <span data-ttu-id="c57e8-109">Esempio 1: ottenere la versione corrente dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="c57e8-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="c57e8-110">Questo comando ottiene la versione corrente dei criteri di conservazione a lungo termine per Database01</span><span class="sxs-lookup"><span data-stu-id="c57e8-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="c57e8-111">Esempio 2: ottenere la versione legacy dei criteri di conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="c57e8-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="c57e8-112">Questo comando ottiene la versione legacy dei criteri di conservazione a lungo termine per Database01</span><span class="sxs-lookup"><span data-stu-id="c57e8-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="c57e8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c57e8-113">PARAMETERS</span></span>

### <span data-ttu-id="c57e8-114">-Current</span><span class="sxs-lookup"><span data-stu-id="c57e8-114">-Current</span></span>
<span data-ttu-id="c57e8-115">Se non viene specificato, il comando restituisce le informazioni sui criteri di conservazione a lungo termine legacy.</span><span class="sxs-lookup"><span data-stu-id="c57e8-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="c57e8-116">In caso contrario, il comando restituisce la versione corrente dei criteri di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="c57e8-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

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

### <span data-ttu-id="c57e8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c57e8-117">-DatabaseName</span></span>
<span data-ttu-id="c57e8-118">Nome del database SQL di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="c57e8-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="c57e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57e8-119">-DefaultProfile</span></span>
<span data-ttu-id="c57e8-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c57e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c57e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="c57e8-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c57e8-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c57e8-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c57e8-123">-ServerName</span></span>
<span data-ttu-id="c57e8-124">Il nome di Azure SQL Server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="c57e8-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="c57e8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c57e8-125">-Confirm</span></span>
<span data-ttu-id="c57e8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c57e8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57e8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57e8-127">-WhatIf</span></span>
<span data-ttu-id="c57e8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c57e8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c57e8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c57e8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57e8-130">CommonParameters</span></span>
<span data-ttu-id="c57e8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c57e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57e8-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c57e8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57e8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c57e8-133">INPUTS</span></span>

### <span data-ttu-id="c57e8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c57e8-134">System.String</span></span>

## <span data-ttu-id="c57e8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c57e8-135">OUTPUTS</span></span>

### <span data-ttu-id="c57e8-136">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c57e8-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c57e8-137">Note</span><span class="sxs-lookup"><span data-stu-id="c57e8-137">NOTES</span></span>

## <span data-ttu-id="c57e8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c57e8-138">RELATED LINKS</span></span>

[<span data-ttu-id="c57e8-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c57e8-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c57e8-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c57e8-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c57e8-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c57e8-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c57e8-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c57e8-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
