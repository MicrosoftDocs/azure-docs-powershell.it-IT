---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180839"
---
# <span data-ttu-id="1324a-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="1324a-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="1324a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1324a-102">SYNOPSIS</span></span>
<span data-ttu-id="1324a-103">Rimuove un'attività servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="1324a-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="1324a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1324a-104">SYNTAX</span></span>

### <span data-ttu-id="1324a-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1324a-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1324a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1324a-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1324a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1324a-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1324a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1324a-108">DESCRIPTION</span></span>
<span data-ttu-id="1324a-109">Il cmdlet Remove-AzDataMigrationTask rimuove un'attività servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="1324a-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="1324a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1324a-110">EXAMPLES</span></span>

### <span data-ttu-id="1324a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1324a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="1324a-112">Nell'esempio precedente viene rimossa un'attività del servizio di migrazione del database di Azure denominata TestTask da Azure in base al parametro del nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1324a-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="1324a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1324a-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="1324a-114">Nell'esempio precedente viene rimossa un'attività servizio di migrazione del database di Azure in base all'oggetto PSProjectTask passato.</span><span class="sxs-lookup"><span data-stu-id="1324a-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="1324a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1324a-115">PARAMETERS</span></span>

### <span data-ttu-id="1324a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1324a-116">-DefaultProfile</span></span>
<span data-ttu-id="1324a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1324a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1324a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1324a-118">-Force</span></span>
<span data-ttu-id="1324a-119">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="1324a-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1324a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1324a-120">-InputObject</span></span>
<span data-ttu-id="1324a-121">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="1324a-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1324a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1324a-122">-Name</span></span>
<span data-ttu-id="1324a-123">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1324a-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1324a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1324a-124">-PassThru</span></span>
<span data-ttu-id="1324a-125">Restituisce vero/falso.</span><span class="sxs-lookup"><span data-stu-id="1324a-125">Returns an true/false.</span></span>
<span data-ttu-id="1324a-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1324a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1324a-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1324a-127">-ProjectName</span></span>
<span data-ttu-id="1324a-128">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="1324a-128">The name of the project.</span></span>

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

### <span data-ttu-id="1324a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1324a-129">-ResourceGroupName</span></span>
<span data-ttu-id="1324a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1324a-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1324a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1324a-131">-ResourceId</span></span>
<span data-ttu-id="1324a-132">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="1324a-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="1324a-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1324a-133">-ServiceName</span></span>
<span data-ttu-id="1324a-134">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="1324a-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="1324a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1324a-135">-Confirm</span></span>
<span data-ttu-id="1324a-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1324a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1324a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1324a-137">-WhatIf</span></span>
<span data-ttu-id="1324a-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1324a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1324a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1324a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1324a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1324a-140">CommonParameters</span></span>
<span data-ttu-id="1324a-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1324a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1324a-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1324a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1324a-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="1324a-143">INPUTS</span></span>

### <span data-ttu-id="1324a-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="1324a-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="1324a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1324a-145">System.String</span></span>

## <span data-ttu-id="1324a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1324a-146">OUTPUTS</span></span>

### <span data-ttu-id="1324a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1324a-147">System.Boolean</span></span>

## <span data-ttu-id="1324a-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="1324a-148">NOTES</span></span>

## <span data-ttu-id="1324a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1324a-149">RELATED LINKS</span></span>
