---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518120"
---
# <span data-ttu-id="ff834-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="ff834-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="ff834-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff834-102">SYNOPSIS</span></span>
<span data-ttu-id="ff834-103">Rimuove un'attività del servizio di migrazione del database Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="ff834-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff834-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff834-104">SYNTAX</span></span>

### <span data-ttu-id="ff834-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff834-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ff834-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff834-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ff834-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff834-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ff834-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff834-108">DESCRIPTION</span></span>
<span data-ttu-id="ff834-109">Il cmdlet Remove-AzureRmDataMigrationTask rimuove un'attività del servizio di migrazione del database Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="ff834-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="ff834-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff834-110">EXAMPLES</span></span>

### <span data-ttu-id="ff834-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff834-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="ff834-112">Nell'esempio precedente viene rimossa un'attività del servizio di migrazione di database di Azure denominata flusso da Azure in base al parametro nome attività.</span><span class="sxs-lookup"><span data-stu-id="ff834-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="ff834-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ff834-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="ff834-114">Nell'esempio precedente viene rimossa un'attività del servizio di migrazione di database di Azure basata sull'oggetto PSProjectTask passato.</span><span class="sxs-lookup"><span data-stu-id="ff834-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="ff834-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff834-115">PARAMETERS</span></span>

### <span data-ttu-id="ff834-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff834-116">-Confirm</span></span>
<span data-ttu-id="ff834-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff834-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff834-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff834-118">-DefaultProfile</span></span>
<span data-ttu-id="ff834-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff834-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff834-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ff834-120">-Force</span></span>
<span data-ttu-id="ff834-121">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="ff834-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff834-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff834-122">-InputObject</span></span>
<span data-ttu-id="ff834-123">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="ff834-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff834-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff834-124">-Name</span></span>
<span data-ttu-id="ff834-125">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ff834-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff834-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff834-126">-PassThru</span></span>
<span data-ttu-id="ff834-127">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="ff834-127">Returns an true/false.</span></span>
<span data-ttu-id="ff834-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ff834-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff834-129">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="ff834-129">-ProjectName</span></span>
<span data-ttu-id="ff834-130">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="ff834-130">The name of the project.</span></span>

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

### <span data-ttu-id="ff834-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff834-131">-ResourceGroupName</span></span>
<span data-ttu-id="ff834-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff834-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff834-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff834-133">-ResourceId</span></span>
<span data-ttu-id="ff834-134">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="ff834-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="ff834-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ff834-135">-ServiceName</span></span>
<span data-ttu-id="ff834-136">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ff834-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="ff834-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff834-137">-WhatIf</span></span>
<span data-ttu-id="ff834-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff834-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff834-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff834-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ff834-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff834-140">INPUTS</span></span>

### <span data-ttu-id="ff834-141">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="ff834-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="ff834-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ff834-142">System.String</span></span>


## <span data-ttu-id="ff834-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff834-143">OUTPUTS</span></span>

### <span data-ttu-id="ff834-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff834-144">System.Boolean</span></span>


## <span data-ttu-id="ff834-145">Note</span><span class="sxs-lookup"><span data-stu-id="ff834-145">NOTES</span></span>

## <span data-ttu-id="ff834-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff834-146">RELATED LINKS</span></span>


