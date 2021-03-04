---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 33bc407c5585017bfe98591649a0c30e46adfea4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955934"
---
# <span data-ttu-id="881b7-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="881b7-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="881b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="881b7-102">SYNOPSIS</span></span>
<span data-ttu-id="881b7-103">Interrompe un'attività del servizio di migrazione del database di Azure in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="881b7-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="881b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="881b7-104">SYNTAX</span></span>

### <span data-ttu-id="881b7-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="881b7-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="881b7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="881b7-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="881b7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="881b7-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="881b7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="881b7-108">DESCRIPTION</span></span>
<span data-ttu-id="881b7-109">Stop-AzDataMigrationTask cmdlet interrompe l'attività di migrazione del database nello stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="881b7-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="881b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="881b7-110">EXAMPLES</span></span>

### <span data-ttu-id="881b7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="881b7-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="881b7-112">L'esempio precedente interrompe l'attività del servizio di migrazione del database di Azure denominata myDMSTask associata al progetto myDMSProject e all'istanza del servizio di migrazione dei database di Azure denominata TestService</span><span class="sxs-lookup"><span data-stu-id="881b7-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="881b7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="881b7-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="881b7-114">L'esempio precedente interrompe l'attività del servizio di migrazione del database di Azure passata come parametro di input OGGETTO PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="881b7-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="881b7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="881b7-115">PARAMETERS</span></span>

### <span data-ttu-id="881b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881b7-116">-DefaultProfile</span></span>
<span data-ttu-id="881b7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="881b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="881b7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="881b7-118">-InputObject</span></span>
<span data-ttu-id="881b7-119">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="881b7-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="881b7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="881b7-120">-Name</span></span>
<span data-ttu-id="881b7-121">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="881b7-121">The name of the task.</span></span>

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

### <span data-ttu-id="881b7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="881b7-122">-PassThru</span></span>
<span data-ttu-id="881b7-123">Restituisce vero/falso.</span><span class="sxs-lookup"><span data-stu-id="881b7-123">Returns an true/false.</span></span>
<span data-ttu-id="881b7-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="881b7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="881b7-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="881b7-125">-ProjectName</span></span>
<span data-ttu-id="881b7-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="881b7-126">The name of the project.</span></span>

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

### <span data-ttu-id="881b7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="881b7-127">-ResourceGroupName</span></span>
<span data-ttu-id="881b7-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="881b7-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="881b7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="881b7-129">-ResourceId</span></span>
<span data-ttu-id="881b7-130">ID risorsa Attività progetto.</span><span class="sxs-lookup"><span data-stu-id="881b7-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="881b7-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="881b7-131">-ServiceName</span></span>
<span data-ttu-id="881b7-132">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="881b7-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="881b7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="881b7-133">-Confirm</span></span>
<span data-ttu-id="881b7-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="881b7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="881b7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="881b7-135">-WhatIf</span></span>
<span data-ttu-id="881b7-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="881b7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="881b7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="881b7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="881b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881b7-138">CommonParameters</span></span>
<span data-ttu-id="881b7-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="881b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881b7-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="881b7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881b7-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="881b7-141">INPUTS</span></span>

### <span data-ttu-id="881b7-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="881b7-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="881b7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="881b7-143">System.String</span></span>

## <span data-ttu-id="881b7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="881b7-144">OUTPUTS</span></span>

### <span data-ttu-id="881b7-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="881b7-145">System.Boolean</span></span>

## <span data-ttu-id="881b7-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="881b7-146">NOTES</span></span>

## <span data-ttu-id="881b7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="881b7-147">RELATED LINKS</span></span>
