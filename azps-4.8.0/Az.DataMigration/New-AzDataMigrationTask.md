---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190775"
---
# <span data-ttu-id="fcde3-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="fcde3-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="fcde3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcde3-102">SYNOPSIS</span></span>
<span data-ttu-id="fcde3-103">Crea e avvia un'attività di migrazione dei dati nel servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="fcde3-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="fcde3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcde3-104">SYNTAX</span></span>

### <span data-ttu-id="fcde3-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fcde3-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcde3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcde3-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcde3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcde3-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcde3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcde3-108">DESCRIPTION</span></span>
<span data-ttu-id="fcde3-109">Il cmdlet New-AzDataMigrationTask crea l'attività di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="fcde3-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="fcde3-110">Questo cmdlet accetta i parametri per l'enumeratore dei tipi di attività, il gruppo di risorse Azure, il nome del servizio di migrazione del database Azure associato e il progetto come input.</span><span class="sxs-lookup"><span data-stu-id="fcde3-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="fcde3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcde3-111">EXAMPLES</span></span>

### <span data-ttu-id="fcde3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fcde3-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="fcde3-113">Questo script di esempio Mostra come creare una nuova attività di migrazione dei dati denominata MyMigrationTask nel progetto denominato myDMSProject e servizio denominato TestService.</span><span class="sxs-lookup"><span data-stu-id="fcde3-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="fcde3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcde3-114">PARAMETERS</span></span>

### <span data-ttu-id="fcde3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcde3-115">-DefaultProfile</span></span>
<span data-ttu-id="fcde3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fcde3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcde3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcde3-117">-InputObject</span></span>
<span data-ttu-id="fcde3-118">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="fcde3-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcde3-119">-Name</span></span>
<span data-ttu-id="fcde3-120">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="fcde3-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="fcde3-121">-ProjectName</span></span>
<span data-ttu-id="fcde3-122">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="fcde3-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcde3-123">-ResourceGroupName</span></span>
<span data-ttu-id="fcde3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fcde3-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcde3-125">-ResourceId</span></span>
<span data-ttu-id="fcde3-126">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="fcde3-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fcde3-127">-ServiceName</span></span>
<span data-ttu-id="fcde3-128">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="fcde3-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="fcde3-129">-TaskType</span></span>
<span data-ttu-id="fcde3-130">Tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="fcde3-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="fcde3-131">-MigrationValidation</span></span> 
<span data-ttu-id="fcde3-132">Oggetto risposta attività tramite chiamata di convalida, facoltativo ma consigliato.</span><span class="sxs-lookup"><span data-stu-id="fcde3-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcde3-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="fcde3-133">-Wait</span></span>
<span data-ttu-id="fcde3-134">Se aspettare che l'attività finisca.</span><span class="sxs-lookup"><span data-stu-id="fcde3-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="fcde3-135">Se il contrassegno è impostato, controlla ogni 1 secondo finché l'attività non termina e restituisce all'utente le proprietà dell'attività in cui è possibile controllare l'output o l'errore.</span><span class="sxs-lookup"><span data-stu-id="fcde3-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="fcde3-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fcde3-136">-Confirm</span></span>
<span data-ttu-id="fcde3-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcde3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcde3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcde3-138">-WhatIf</span></span>
<span data-ttu-id="fcde3-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcde3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcde3-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcde3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcde3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcde3-141">CommonParameters</span></span>
<span data-ttu-id="fcde3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcde3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcde3-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcde3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcde3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcde3-144">INPUTS</span></span>

### <span data-ttu-id="fcde3-145">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="fcde3-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="fcde3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fcde3-146">System.String</span></span>

## <span data-ttu-id="fcde3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcde3-147">OUTPUTS</span></span>

### <span data-ttu-id="fcde3-148">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="fcde3-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="fcde3-149">Note</span><span class="sxs-lookup"><span data-stu-id="fcde3-149">NOTES</span></span>

## <span data-ttu-id="fcde3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcde3-150">RELATED LINKS</span></span>
