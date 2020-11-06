---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 5aada0f82b8d2a11486e3dde2f4b806f735979e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520633"
---
# <span data-ttu-id="2308b-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2308b-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="2308b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2308b-102">SYNOPSIS</span></span>
<span data-ttu-id="2308b-103">Rimuove un progetto di servizio di migrazione di database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="2308b-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2308b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2308b-104">SYNTAX</span></span>

### <span data-ttu-id="2308b-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2308b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2308b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2308b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2308b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2308b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2308b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2308b-108">DESCRIPTION</span></span>
<span data-ttu-id="2308b-109">Il cmdlet Remove-AzureRmDataMigrationProject rimuove un progetto di servizio di migrazione di database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="2308b-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="2308b-110">Fornendo il parametro DeleteRunningTask, vengono rimosse tutte le attività del servizio di migrazione del database di Azure associate al progetto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2308b-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="2308b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2308b-111">EXAMPLES</span></span>

### <span data-ttu-id="2308b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2308b-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="2308b-113">Nell'esempio precedente viene rimosso il progetto del servizio di migrazione del database di Azure denominato myDMProject da Azure in base al nome come parametro di input</span><span class="sxs-lookup"><span data-stu-id="2308b-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="2308b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2308b-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="2308b-115">Nell'esempio precedente viene rimosso il progetto del servizio di migrazione del database di Azure basato sull'oggetto PSProject come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="2308b-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="2308b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2308b-116">PARAMETERS</span></span>

### <span data-ttu-id="2308b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2308b-117">-DefaultProfile</span></span>
<span data-ttu-id="2308b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2308b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2308b-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="2308b-119">-DeleteRunningTask</span></span>
<span data-ttu-id="2308b-120">Eliminare qualsiasi attività in corso</span><span class="sxs-lookup"><span data-stu-id="2308b-120">Delete any running task</span></span>

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

### <span data-ttu-id="2308b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2308b-121">-Force</span></span>
<span data-ttu-id="2308b-122">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="2308b-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2308b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2308b-123">-InputObject</span></span>
<span data-ttu-id="2308b-124">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="2308b-124">PSProject Object.</span></span>

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

### <span data-ttu-id="2308b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2308b-125">-Name</span></span>
<span data-ttu-id="2308b-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="2308b-126">The name of the project.</span></span>

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

### <span data-ttu-id="2308b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2308b-127">-PassThru</span></span>
<span data-ttu-id="2308b-128">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="2308b-128">Returns an true/false.</span></span>
<span data-ttu-id="2308b-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2308b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2308b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2308b-130">-ResourceGroupName</span></span>
<span data-ttu-id="2308b-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2308b-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="2308b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2308b-132">-ResourceId</span></span>
<span data-ttu-id="2308b-133">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="2308b-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="2308b-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2308b-134">-ServiceName</span></span>
<span data-ttu-id="2308b-135">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="2308b-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2308b-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2308b-136">-Confirm</span></span>
<span data-ttu-id="2308b-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2308b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2308b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2308b-138">-WhatIf</span></span>
<span data-ttu-id="2308b-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2308b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2308b-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2308b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2308b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2308b-141">CommonParameters</span></span>
<span data-ttu-id="2308b-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2308b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2308b-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2308b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2308b-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2308b-144">INPUTS</span></span>

### <span data-ttu-id="2308b-145">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2308b-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="2308b-146">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2308b-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2308b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2308b-147">System.String</span></span>

## <span data-ttu-id="2308b-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2308b-148">OUTPUTS</span></span>

### <span data-ttu-id="2308b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2308b-149">System.Boolean</span></span>

## <span data-ttu-id="2308b-150">Note</span><span class="sxs-lookup"><span data-stu-id="2308b-150">NOTES</span></span>

## <span data-ttu-id="2308b-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2308b-151">RELATED LINKS</span></span>
