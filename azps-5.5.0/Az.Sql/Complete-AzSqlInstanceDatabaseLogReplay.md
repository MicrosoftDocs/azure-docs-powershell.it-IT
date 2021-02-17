---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196254"
---
# <span data-ttu-id="b2e17-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="b2e17-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="b2e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e17-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e17-103">Completa il servizio di riproduzione del log per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="b2e17-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="b2e17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2e17-104">SYNTAX</span></span>

### <span data-ttu-id="b2e17-105">LogReplayInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2e17-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e17-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b2e17-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e17-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2e17-107">DESCRIPTION</span></span>
<span data-ttu-id="b2e17-108">Il cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** completa il servizio di riproduzione del log nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="b2e17-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="b2e17-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2e17-109">EXAMPLES</span></span>

### <span data-ttu-id="b2e17-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2e17-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="b2e17-111">Questo comando completa il servizio di riproduzione del log per il database specificato dopo il ripristino dell'ultimo backup.</span><span class="sxs-lookup"><span data-stu-id="b2e17-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="b2e17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e17-112">PARAMETERS</span></span>

### <span data-ttu-id="b2e17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e17-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e17-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e17-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2e17-115">-InputObject</span></span>
<span data-ttu-id="b2e17-116">Oggetto di database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b2e17-116">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b2e17-117">-InstanceName</span></span>
<span data-ttu-id="b2e17-118">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b2e17-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="b2e17-119">-LastBackupName</span></span>
<span data-ttu-id="b2e17-120">Nome dell'ultimo file di backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="b2e17-120">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e17-121">-Name</span></span>
<span data-ttu-id="b2e17-122">Nome del database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b2e17-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2e17-123">-PassThru</span></span>
<span data-ttu-id="b2e17-124">Definisce se restituire il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b2e17-124">Defines Whether return the sync group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e17-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2e17-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2e17-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e17-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2e17-127">-Confirm</span></span>
<span data-ttu-id="b2e17-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e17-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e17-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e17-129">-WhatIf</span></span>
<span data-ttu-id="b2e17-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e17-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2e17-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e17-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e17-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e17-132">CommonParameters</span></span>
<span data-ttu-id="b2e17-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e17-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e17-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2e17-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e17-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2e17-135">INPUTS</span></span>

### <span data-ttu-id="b2e17-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b2e17-136">System.String</span></span>

### <span data-ttu-id="b2e17-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b2e17-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b2e17-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2e17-138">OUTPUTS</span></span>

## <span data-ttu-id="b2e17-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2e17-139">NOTES</span></span>

## <span data-ttu-id="b2e17-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2e17-140">RELATED LINKS</span></span>
