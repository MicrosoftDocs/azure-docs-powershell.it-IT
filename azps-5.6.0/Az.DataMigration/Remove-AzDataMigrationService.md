---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996770"
---
# <span data-ttu-id="c524c-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c524c-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="c524c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c524c-102">SYNOPSIS</span></span>
<span data-ttu-id="c524c-103">Rimuove un'istanza del servizio di migrazione dei database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="c524c-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="c524c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c524c-104">SYNTAX</span></span>

### <span data-ttu-id="c524c-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c524c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c524c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c524c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c524c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c524c-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c524c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c524c-108">DESCRIPTION</span></span>
<span data-ttu-id="c524c-109">Il cmdlet Remove-AzDataMigrationService rimuove un'istanza del servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="c524c-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="c524c-110">Se si specifica il parametro DeleteRunningTask, vengono rimosse tutte le attività del servizio di migrazione del database di Azure associate al servizio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c524c-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="c524c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c524c-111">EXAMPLES</span></span>

### <span data-ttu-id="c524c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c524c-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="c524c-113">L'esempio precedente rimuove un'istanza del servizio di migrazione del database di Azure denominata TestService contenuta in un gruppo di risorse di Azure denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c524c-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="c524c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c524c-114">PARAMETERS</span></span>

### <span data-ttu-id="c524c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c524c-115">-DefaultProfile</span></span>
<span data-ttu-id="c524c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c524c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c524c-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="c524c-117">-DeleteRunningTask</span></span>
<span data-ttu-id="c524c-118">Eliminare qualsiasi attività in esecuzione</span><span class="sxs-lookup"><span data-stu-id="c524c-118">Delete any running task</span></span>

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

### <span data-ttu-id="c524c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c524c-119">-Force</span></span>
<span data-ttu-id="c524c-120">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="c524c-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c524c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c524c-121">-InputObject</span></span>
<span data-ttu-id="c524c-122">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="c524c-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c524c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c524c-123">-Name</span></span>
<span data-ttu-id="c524c-124">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="c524c-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c524c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c524c-125">-PassThru</span></span>
<span data-ttu-id="c524c-126">Restituisce vero/falso.</span><span class="sxs-lookup"><span data-stu-id="c524c-126">Returns an true/false.</span></span>
<span data-ttu-id="c524c-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c524c-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c524c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c524c-128">-ResourceGroupName</span></span>
<span data-ttu-id="c524c-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c524c-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c524c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c524c-130">-ResourceId</span></span>
<span data-ttu-id="c524c-131">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="c524c-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="c524c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c524c-132">-Confirm</span></span>
<span data-ttu-id="c524c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c524c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c524c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c524c-134">-WhatIf</span></span>
<span data-ttu-id="c524c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c524c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c524c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c524c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c524c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c524c-137">CommonParameters</span></span>
<span data-ttu-id="c524c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c524c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c524c-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c524c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c524c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="c524c-140">INPUTS</span></span>

### <span data-ttu-id="c524c-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c524c-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="c524c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c524c-142">System.String</span></span>

## <span data-ttu-id="c524c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c524c-143">OUTPUTS</span></span>

### <span data-ttu-id="c524c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c524c-144">System.Boolean</span></span>

## <span data-ttu-id="c524c-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="c524c-145">NOTES</span></span>

## <span data-ttu-id="c524c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c524c-146">RELATED LINKS</span></span>
