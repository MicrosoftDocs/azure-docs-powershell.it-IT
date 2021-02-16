---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201526"
---
# <span data-ttu-id="1dd18-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1dd18-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="1dd18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd18-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd18-103">Ottiene i criteri di conservazione a lungo termine di un database gestito</span><span class="sxs-lookup"><span data-stu-id="1dd18-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="1dd18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dd18-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dd18-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dd18-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd18-106">Il cmdlet **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** ottiene i criteri di conservazione a lungo termine registrati nel database gestito.</span><span class="sxs-lookup"><span data-stu-id="1dd18-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="1dd18-107">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="1dd18-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="1dd18-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dd18-108">EXAMPLES</span></span>

### <span data-ttu-id="1dd18-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dd18-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="1dd18-110">Ottiene la versione corrente dei criteri di conservazione a lungo termine per il database</span><span class="sxs-lookup"><span data-stu-id="1dd18-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="1dd18-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dd18-111">PARAMETERS</span></span>

### <span data-ttu-id="1dd18-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dd18-112">-DatabaseName</span></span>
<span data-ttu-id="1dd18-113">Nome del database gestito di Azure da usare.</span><span class="sxs-lookup"><span data-stu-id="1dd18-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="1dd18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd18-114">-DefaultProfile</span></span>
<span data-ttu-id="1dd18-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd18-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1dd18-116">-InstanceName</span></span>
<span data-ttu-id="1dd18-117">Il nome dell'istanza gestita di Azure a cui appartiene il database.</span><span class="sxs-lookup"><span data-stu-id="1dd18-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="1dd18-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd18-118">-ResourceGroupName</span></span>
<span data-ttu-id="1dd18-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dd18-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dd18-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dd18-120">-Confirm</span></span>
<span data-ttu-id="1dd18-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dd18-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd18-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd18-122">-WhatIf</span></span>
<span data-ttu-id="1dd18-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd18-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd18-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd18-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd18-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd18-125">CommonParameters</span></span>
<span data-ttu-id="1dd18-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd18-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd18-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1dd18-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd18-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dd18-128">INPUTS</span></span>

### <span data-ttu-id="1dd18-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1dd18-129">System.String</span></span>

## <span data-ttu-id="1dd18-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dd18-130">OUTPUTS</span></span>

### <span data-ttu-id="1dd18-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1dd18-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="1dd18-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dd18-132">NOTES</span></span>

## <span data-ttu-id="1dd18-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dd18-133">RELATED LINKS</span></span>

[<span data-ttu-id="1dd18-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1dd18-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1dd18-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1dd18-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1dd18-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1dd18-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1dd18-137">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="1dd18-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)