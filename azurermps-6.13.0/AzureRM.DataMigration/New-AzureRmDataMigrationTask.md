---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520636"
---
# <span data-ttu-id="e1d30-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e1d30-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="e1d30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1d30-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d30-103">Crea e avvia un'attività di migrazione dei dati nel servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d30-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1d30-104">SYNTAX</span></span>

### <span data-ttu-id="e1d30-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1d30-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1d30-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d30-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1d30-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1d30-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1d30-108">DESCRIPTION</span></span>
<span data-ttu-id="e1d30-109">Il cmdlet New-AzureRmDataMigrationTask crea l'attività di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="e1d30-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="e1d30-110">Questo cmdlet accetta i parametri per l'enumeratore dei tipi di attività, il gruppo di risorse Azure, il nome del servizio di migrazione del database Azure associato e il progetto come input.</span><span class="sxs-lookup"><span data-stu-id="e1d30-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="e1d30-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1d30-111">EXAMPLES</span></span>

### <span data-ttu-id="e1d30-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1d30-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="e1d30-113">Questo script di esempio Mostra come creare una nuova attività di migrazione dei dati denominata MyMigrationTask nel progetto denominato myDMSProject e servizio denominato TestService.</span><span class="sxs-lookup"><span data-stu-id="e1d30-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="e1d30-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1d30-114">PARAMETERS</span></span>

### <span data-ttu-id="e1d30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d30-115">-DefaultProfile</span></span>
<span data-ttu-id="e1d30-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d30-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1d30-117">-InputObject</span></span>
<span data-ttu-id="e1d30-118">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="e1d30-118">PSProject Object.</span></span>

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

### <span data-ttu-id="e1d30-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1d30-119">-Name</span></span>
<span data-ttu-id="e1d30-120">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e1d30-120">The name of the task.</span></span>

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

### <span data-ttu-id="e1d30-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="e1d30-121">-ProjectName</span></span>
<span data-ttu-id="e1d30-122">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="e1d30-122">The name of the project.</span></span>

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

### <span data-ttu-id="e1d30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d30-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1d30-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1d30-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e1d30-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1d30-125">-ResourceId</span></span>
<span data-ttu-id="e1d30-126">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="e1d30-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="e1d30-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e1d30-127">-ServiceName</span></span>
<span data-ttu-id="e1d30-128">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="e1d30-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e1d30-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="e1d30-129">-TaskType</span></span>
<span data-ttu-id="e1d30-130">Tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="e1d30-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d30-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1d30-131">-Confirm</span></span>
<span data-ttu-id="e1d30-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1d30-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d30-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d30-133">-WhatIf</span></span>
<span data-ttu-id="e1d30-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1d30-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d30-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1d30-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d30-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d30-136">CommonParameters</span></span>
<span data-ttu-id="e1d30-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d30-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d30-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d30-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d30-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1d30-139">INPUTS</span></span>

### <span data-ttu-id="e1d30-140">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="e1d30-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="e1d30-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e1d30-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e1d30-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e1d30-142">System.String</span></span>

## <span data-ttu-id="e1d30-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1d30-143">OUTPUTS</span></span>

### <span data-ttu-id="e1d30-144">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="e1d30-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="e1d30-145">Note</span><span class="sxs-lookup"><span data-stu-id="e1d30-145">NOTES</span></span>

## <span data-ttu-id="e1d30-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1d30-146">RELATED LINKS</span></span>
