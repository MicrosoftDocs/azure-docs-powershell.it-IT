---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686111"
---
# <span data-ttu-id="62a13-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="62a13-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="62a13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62a13-102">SYNOPSIS</span></span>
<span data-ttu-id="62a13-103">Crea e avvia un'attività di migrazione dei dati nel servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="62a13-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62a13-104">SYNTAX</span></span>

### <span data-ttu-id="62a13-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62a13-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62a13-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a13-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62a13-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62a13-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="62a13-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62a13-108">DESCRIPTION</span></span>
<span data-ttu-id="62a13-109">Il cmdlet New-AzureRmDataMigrationTask crea l'attività di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="62a13-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="62a13-110">Questo cmdlet accetta i parametri per l'enumeratore dei tipi di attività, il gruppo di risorse Azure, il nome del servizio di migrazione dei dati di Azure associato e il progetto come input.</span><span class="sxs-lookup"><span data-stu-id="62a13-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="62a13-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62a13-111">EXAMPLES</span></span>

### <span data-ttu-id="62a13-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62a13-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="62a13-113">Questo script di esempio Mostra come creare una nuova attività di migrazione dei dati denominata MyMigrationTask nel progetto denominato myDMSProject e servizio denominato TestService.</span><span class="sxs-lookup"><span data-stu-id="62a13-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="62a13-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62a13-114">PARAMETERS</span></span>

### <span data-ttu-id="62a13-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62a13-115">-Confirm</span></span>
<span data-ttu-id="62a13-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a13-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a13-117">-DefaultProfile</span></span>
<span data-ttu-id="62a13-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62a13-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62a13-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62a13-119">-InputObject</span></span>
<span data-ttu-id="62a13-120">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="62a13-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="62a13-121">-Name</span></span>
<span data-ttu-id="62a13-122">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="62a13-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-123">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="62a13-123">-ProjectName</span></span>
<span data-ttu-id="62a13-124">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="62a13-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a13-125">-ResourceGroupName</span></span>
<span data-ttu-id="62a13-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62a13-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62a13-127">-ResourceId</span></span>
<span data-ttu-id="62a13-128">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="62a13-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="62a13-129">-ServiceName</span></span>
<span data-ttu-id="62a13-130">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="62a13-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="62a13-131">-TaskType</span></span>
<span data-ttu-id="62a13-132">Tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="62a13-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a13-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a13-133">-WhatIf</span></span>
<span data-ttu-id="62a13-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62a13-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a13-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62a13-135">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="62a13-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62a13-136">INPUTS</span></span>

### <span data-ttu-id="62a13-137">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="62a13-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="62a13-138">System. String</span><span class="sxs-lookup"><span data-stu-id="62a13-138">System.String</span></span>


## <span data-ttu-id="62a13-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62a13-139">OUTPUTS</span></span>

### <span data-ttu-id="62a13-140">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="62a13-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="62a13-141">Note</span><span class="sxs-lookup"><span data-stu-id="62a13-141">NOTES</span></span>

## <span data-ttu-id="62a13-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62a13-142">RELATED LINKS</span></span>


