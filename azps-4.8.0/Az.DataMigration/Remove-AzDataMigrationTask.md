---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192534"
---
# <span data-ttu-id="929cc-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="929cc-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="929cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="929cc-102">SYNOPSIS</span></span>
<span data-ttu-id="929cc-103">Rimuove un'attività del servizio di migrazione del database Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="929cc-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="929cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="929cc-104">SYNTAX</span></span>

### <span data-ttu-id="929cc-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="929cc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="929cc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="929cc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="929cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="929cc-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="929cc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="929cc-108">DESCRIPTION</span></span>
<span data-ttu-id="929cc-109">Il cmdlet Remove-AzDataMigrationTask rimuove un'attività del servizio di migrazione del database Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="929cc-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="929cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="929cc-110">EXAMPLES</span></span>

### <span data-ttu-id="929cc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="929cc-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="929cc-112">Nell'esempio precedente viene rimossa un'attività del servizio di migrazione di database di Azure denominata flusso da Azure in base al parametro nome attività.</span><span class="sxs-lookup"><span data-stu-id="929cc-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="929cc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="929cc-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="929cc-114">Nell'esempio precedente viene rimossa un'attività del servizio di migrazione di database di Azure basata sull'oggetto PSProjectTask passato.</span><span class="sxs-lookup"><span data-stu-id="929cc-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="929cc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="929cc-115">PARAMETERS</span></span>

### <span data-ttu-id="929cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929cc-116">-DefaultProfile</span></span>
<span data-ttu-id="929cc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="929cc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="929cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="929cc-118">-Force</span></span>
<span data-ttu-id="929cc-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="929cc-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="929cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="929cc-120">-InputObject</span></span>
<span data-ttu-id="929cc-121">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="929cc-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="929cc-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="929cc-122">-Name</span></span>
<span data-ttu-id="929cc-123">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="929cc-123">The name of the task.</span></span>

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

### <span data-ttu-id="929cc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="929cc-124">-PassThru</span></span>
<span data-ttu-id="929cc-125">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="929cc-125">Returns an true/false.</span></span>
<span data-ttu-id="929cc-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="929cc-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="929cc-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="929cc-127">-ProjectName</span></span>
<span data-ttu-id="929cc-128">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="929cc-128">The name of the project.</span></span>

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

### <span data-ttu-id="929cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="929cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="929cc-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="929cc-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="929cc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="929cc-131">-ResourceId</span></span>
<span data-ttu-id="929cc-132">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="929cc-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="929cc-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="929cc-133">-ServiceName</span></span>
<span data-ttu-id="929cc-134">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="929cc-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="929cc-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="929cc-135">-Confirm</span></span>
<span data-ttu-id="929cc-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="929cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929cc-137">-WhatIf</span></span>
<span data-ttu-id="929cc-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="929cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="929cc-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="929cc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929cc-140">CommonParameters</span></span>
<span data-ttu-id="929cc-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="929cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929cc-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929cc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929cc-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="929cc-143">INPUTS</span></span>

### <span data-ttu-id="929cc-144">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="929cc-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="929cc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="929cc-145">System.String</span></span>

## <span data-ttu-id="929cc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="929cc-146">OUTPUTS</span></span>

### <span data-ttu-id="929cc-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="929cc-147">System.Boolean</span></span>

## <span data-ttu-id="929cc-148">Note</span><span class="sxs-lookup"><span data-stu-id="929cc-148">NOTES</span></span>

## <span data-ttu-id="929cc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="929cc-149">RELATED LINKS</span></span>