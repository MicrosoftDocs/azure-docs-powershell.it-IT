---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 53dc4841dbbdcb7f3d855630b69a94320b4dfeff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674718"
---
# <span data-ttu-id="122f9-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="122f9-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="122f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="122f9-102">SYNOPSIS</span></span>
<span data-ttu-id="122f9-103">Rimuove un progetto di servizio di migrazione di database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="122f9-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="122f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="122f9-104">SYNTAX</span></span>

### <span data-ttu-id="122f9-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="122f9-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122f9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="122f9-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122f9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="122f9-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122f9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="122f9-108">DESCRIPTION</span></span>
<span data-ttu-id="122f9-109">Il cmdlet Remove-AzDataMigrationProject rimuove un progetto di servizio di migrazione di database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="122f9-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="122f9-110">Fornendo il parametro DeleteRunningTask, vengono rimosse tutte le attività del servizio di migrazione del database di Azure associate al progetto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="122f9-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="122f9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="122f9-111">EXAMPLES</span></span>

### <span data-ttu-id="122f9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="122f9-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="122f9-113">Nell'esempio precedente viene rimosso il progetto del servizio di migrazione del database di Azure denominato myDMProject da Azure in base al nome come parametro di input</span><span class="sxs-lookup"><span data-stu-id="122f9-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="122f9-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="122f9-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="122f9-115">Nell'esempio precedente viene rimosso il progetto del servizio di migrazione del database di Azure basato sull'oggetto PSProject come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="122f9-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="122f9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="122f9-116">PARAMETERS</span></span>

### <span data-ttu-id="122f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122f9-117">-DefaultProfile</span></span>
<span data-ttu-id="122f9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="122f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="122f9-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="122f9-119">-DeleteRunningTask</span></span>
<span data-ttu-id="122f9-120">Eliminare qualsiasi attività in corso</span><span class="sxs-lookup"><span data-stu-id="122f9-120">Delete any running task</span></span>

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

### <span data-ttu-id="122f9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="122f9-121">-Force</span></span>
<span data-ttu-id="122f9-122">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="122f9-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="122f9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="122f9-123">-InputObject</span></span>
<span data-ttu-id="122f9-124">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="122f9-124">PSProject Object.</span></span>

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

### <span data-ttu-id="122f9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="122f9-125">-Name</span></span>
<span data-ttu-id="122f9-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="122f9-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="122f9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="122f9-127">-PassThru</span></span>
<span data-ttu-id="122f9-128">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="122f9-128">Returns an true/false.</span></span>
<span data-ttu-id="122f9-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="122f9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="122f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="122f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="122f9-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="122f9-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="122f9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="122f9-132">-ResourceId</span></span>
<span data-ttu-id="122f9-133">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="122f9-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="122f9-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="122f9-134">-ServiceName</span></span>
<span data-ttu-id="122f9-135">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="122f9-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="122f9-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="122f9-136">-Confirm</span></span>
<span data-ttu-id="122f9-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="122f9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="122f9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122f9-138">-WhatIf</span></span>
<span data-ttu-id="122f9-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="122f9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="122f9-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="122f9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="122f9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122f9-141">CommonParameters</span></span>
<span data-ttu-id="122f9-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122f9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122f9-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122f9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122f9-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="122f9-144">INPUTS</span></span>

### <span data-ttu-id="122f9-145">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="122f9-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="122f9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="122f9-146">System.String</span></span>

## <span data-ttu-id="122f9-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="122f9-147">OUTPUTS</span></span>

### <span data-ttu-id="122f9-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="122f9-148">System.Boolean</span></span>

## <span data-ttu-id="122f9-149">Note</span><span class="sxs-lookup"><span data-stu-id="122f9-149">NOTES</span></span>

## <span data-ttu-id="122f9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="122f9-150">RELATED LINKS</span></span>