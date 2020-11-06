---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521045"
---
# <span data-ttu-id="711f4-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="711f4-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="711f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="711f4-102">SYNOPSIS</span></span>
<span data-ttu-id="711f4-103">Rimuove un progetto di servizio di migrazione di database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="711f4-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="711f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="711f4-104">SYNTAX</span></span>

### <span data-ttu-id="711f4-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="711f4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="711f4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="711f4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="711f4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="711f4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="711f4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="711f4-108">DESCRIPTION</span></span>
<span data-ttu-id="711f4-109">Il cmdlet Remove-AzureRmDataMigrationProject rimuove un progetto di servizio di migrazione di database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="711f4-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="711f4-110">Fornendo il parametro DeleteRunningTask, vengono rimosse tutte le attività del servizio di migrazione del database di Azure associate al progetto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="711f4-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="711f4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="711f4-111">EXAMPLES</span></span>

### <span data-ttu-id="711f4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="711f4-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="711f4-113">Nell'esempio precedente viene rimosso il progetto del servizio di migrazione del database di Azure denominato myDMProject da Azure in base al nome come parametro di input</span><span class="sxs-lookup"><span data-stu-id="711f4-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="711f4-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="711f4-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="711f4-115">Nell'esempio precedente viene rimosso il progetto del servizio di migrazione del database di Azure basato sull'oggetto PSProject come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="711f4-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="711f4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="711f4-116">PARAMETERS</span></span>

### <span data-ttu-id="711f4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="711f4-117">-Confirm</span></span>
<span data-ttu-id="711f4-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="711f4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711f4-119">-DefaultProfile</span></span>
<span data-ttu-id="711f4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="711f4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="711f4-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="711f4-121">-DeleteRunningTask</span></span>
<span data-ttu-id="711f4-122">Eliminare qualsiasi attività in corso</span><span class="sxs-lookup"><span data-stu-id="711f4-122">Delete any running task</span></span>

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

### <span data-ttu-id="711f4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="711f4-123">-Force</span></span>
<span data-ttu-id="711f4-124">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="711f4-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="711f4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="711f4-125">-InputObject</span></span>
<span data-ttu-id="711f4-126">Oggetto PSProject.</span><span class="sxs-lookup"><span data-stu-id="711f4-126">PSProject Object.</span></span>

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

### <span data-ttu-id="711f4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="711f4-127">-Name</span></span>
<span data-ttu-id="711f4-128">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="711f4-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711f4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="711f4-129">-PassThru</span></span>
<span data-ttu-id="711f4-130">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="711f4-130">Returns an true/false.</span></span>
<span data-ttu-id="711f4-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="711f4-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="711f4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711f4-132">-ResourceGroupName</span></span>
<span data-ttu-id="711f4-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="711f4-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="711f4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="711f4-134">-ResourceId</span></span>
<span data-ttu-id="711f4-135">ID risorsa progetto.</span><span class="sxs-lookup"><span data-stu-id="711f4-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="711f4-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="711f4-136">-ServiceName</span></span>
<span data-ttu-id="711f4-137">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="711f4-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="711f4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711f4-138">-WhatIf</span></span>
<span data-ttu-id="711f4-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="711f4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711f4-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="711f4-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="711f4-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="711f4-141">INPUTS</span></span>

### <span data-ttu-id="711f4-142">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="711f4-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="711f4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="711f4-143">System.String</span></span>


## <span data-ttu-id="711f4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="711f4-144">OUTPUTS</span></span>

### <span data-ttu-id="711f4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="711f4-145">System.Boolean</span></span>


## <span data-ttu-id="711f4-146">Note</span><span class="sxs-lookup"><span data-stu-id="711f4-146">NOTES</span></span>

## <span data-ttu-id="711f4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="711f4-147">RELATED LINKS</span></span>

