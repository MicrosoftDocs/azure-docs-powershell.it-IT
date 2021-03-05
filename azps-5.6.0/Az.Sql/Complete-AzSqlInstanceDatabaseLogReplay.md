---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2237522cbf7b179358ea4fa9f7ed7608222782ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011581"
---
# <span data-ttu-id="bc8cf-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="bc8cf-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="bc8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8cf-103">Completa il servizio di riproduzione del log per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="bc8cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc8cf-104">SYNTAX</span></span>

### <span data-ttu-id="bc8cf-105">LogReplayInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc8cf-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc8cf-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="bc8cf-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc8cf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc8cf-107">DESCRIPTION</span></span>
<span data-ttu-id="bc8cf-108">Il cmdlet **Complete-AzSqlInstanceDatabaseLogReplay** completa il servizio di riproduzione del log nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="bc8cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc8cf-109">EXAMPLES</span></span>

### <span data-ttu-id="bc8cf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc8cf-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="bc8cf-111">Questo comando completa il servizio di riproduzione del log per il database specificato dopo il ripristino dell'ultimo backup.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="bc8cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc8cf-112">PARAMETERS</span></span>

### <span data-ttu-id="bc8cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8cf-113">-DefaultProfile</span></span>
<span data-ttu-id="bc8cf-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc8cf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc8cf-115">-InputObject</span></span>
<span data-ttu-id="bc8cf-116">Oggetto di database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-116">The instance database object.</span></span>

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

### <span data-ttu-id="bc8cf-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bc8cf-117">-InstanceName</span></span>
<span data-ttu-id="bc8cf-118">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-118">The name of the instance.</span></span>

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

### <span data-ttu-id="bc8cf-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="bc8cf-119">-LastBackupName</span></span>
<span data-ttu-id="bc8cf-120">Nome dell'ultimo file di backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="bc8cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bc8cf-121">-Name</span></span>
<span data-ttu-id="bc8cf-122">Nome del database dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="bc8cf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc8cf-123">-PassThru</span></span>
<span data-ttu-id="bc8cf-124">Definisce se restituire il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="bc8cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc8cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc8cf-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="bc8cf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc8cf-127">-Confirm</span></span>
<span data-ttu-id="bc8cf-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc8cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc8cf-129">-WhatIf</span></span>
<span data-ttu-id="bc8cf-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc8cf-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc8cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8cf-132">CommonParameters</span></span>
<span data-ttu-id="bc8cf-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8cf-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc8cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8cf-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc8cf-135">INPUTS</span></span>

### <span data-ttu-id="bc8cf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bc8cf-136">System.String</span></span>

### <span data-ttu-id="bc8cf-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bc8cf-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="bc8cf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc8cf-138">OUTPUTS</span></span>

## <span data-ttu-id="bc8cf-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc8cf-139">NOTES</span></span>

## <span data-ttu-id="bc8cf-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc8cf-140">RELATED LINKS</span></span>
