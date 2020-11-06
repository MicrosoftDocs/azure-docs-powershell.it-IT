---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519020"
---
# <span data-ttu-id="0642f-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0642f-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="0642f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0642f-102">SYNOPSIS</span></span>
<span data-ttu-id="0642f-103">Rimuove un'istanza del servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="0642f-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0642f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0642f-104">SYNTAX</span></span>

### <span data-ttu-id="0642f-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0642f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0642f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0642f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0642f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0642f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0642f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0642f-108">DESCRIPTION</span></span>
<span data-ttu-id="0642f-109">Il cmdlet Remove-AzureRmDataMigrationService consente di rimuovere un'istanza del servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="0642f-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="0642f-110">Fornendo il parametro DeleteRunningTask, vengono rimosse tutte le attività del servizio di migrazione del database di Azure associate al servizio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0642f-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="0642f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0642f-111">EXAMPLES</span></span>

### <span data-ttu-id="0642f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0642f-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="0642f-113">Nell'esempio precedente viene rimossa un'istanza del servizio di migrazione del database di Azure denominata TestService contenuta in un gruppo di risorse Azure denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0642f-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="0642f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0642f-114">PARAMETERS</span></span>

### <span data-ttu-id="0642f-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0642f-115">-Confirm</span></span>
<span data-ttu-id="0642f-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0642f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0642f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0642f-117">-DefaultProfile</span></span>
<span data-ttu-id="0642f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0642f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0642f-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="0642f-119">-DeleteRunningTask</span></span>
<span data-ttu-id="0642f-120">Eliminare qualsiasi attività in corso</span><span class="sxs-lookup"><span data-stu-id="0642f-120">Delete any running task</span></span>

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

### <span data-ttu-id="0642f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0642f-121">-Force</span></span>
<span data-ttu-id="0642f-122">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="0642f-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0642f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0642f-123">-InputObject</span></span>
<span data-ttu-id="0642f-124">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="0642f-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0642f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0642f-125">-Name</span></span>
<span data-ttu-id="0642f-126">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0642f-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0642f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0642f-127">-PassThru</span></span>
<span data-ttu-id="0642f-128">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="0642f-128">Returns an true/false.</span></span>
<span data-ttu-id="0642f-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0642f-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0642f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0642f-130">-ResourceGroupName</span></span>
<span data-ttu-id="0642f-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0642f-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="0642f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0642f-132">-ResourceId</span></span>
<span data-ttu-id="0642f-133">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="0642f-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="0642f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0642f-134">-WhatIf</span></span>
<span data-ttu-id="0642f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0642f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0642f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0642f-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="0642f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0642f-137">INPUTS</span></span>

### <span data-ttu-id="0642f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0642f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="0642f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0642f-139">System.String</span></span>


## <span data-ttu-id="0642f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0642f-140">OUTPUTS</span></span>

### <span data-ttu-id="0642f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0642f-141">System.Boolean</span></span>


## <span data-ttu-id="0642f-142">Note</span><span class="sxs-lookup"><span data-stu-id="0642f-142">NOTES</span></span>

## <span data-ttu-id="0642f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0642f-143">RELATED LINKS</span></span>


