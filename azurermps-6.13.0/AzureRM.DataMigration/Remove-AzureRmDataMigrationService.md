---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520634"
---
# <span data-ttu-id="639fa-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="639fa-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="639fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="639fa-102">SYNOPSIS</span></span>
<span data-ttu-id="639fa-103">Rimuove un'istanza del servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="639fa-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="639fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="639fa-104">SYNTAX</span></span>

### <span data-ttu-id="639fa-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="639fa-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="639fa-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="639fa-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="639fa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="639fa-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="639fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="639fa-108">DESCRIPTION</span></span>
<span data-ttu-id="639fa-109">Il cmdlet Remove-AzureRmDataMigrationService consente di rimuovere un'istanza del servizio di migrazione del database di Azure da Azure.</span><span class="sxs-lookup"><span data-stu-id="639fa-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="639fa-110">Fornendo il parametro DeleteRunningTask, vengono rimosse tutte le attività del servizio di migrazione del database di Azure associate al servizio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="639fa-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="639fa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="639fa-111">EXAMPLES</span></span>

### <span data-ttu-id="639fa-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="639fa-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="639fa-113">Nell'esempio precedente viene rimossa un'istanza del servizio di migrazione del database di Azure denominata TestService contenuta in un gruppo di risorse Azure denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="639fa-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="639fa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="639fa-114">PARAMETERS</span></span>

### <span data-ttu-id="639fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639fa-115">-DefaultProfile</span></span>
<span data-ttu-id="639fa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="639fa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="639fa-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="639fa-117">-DeleteRunningTask</span></span>
<span data-ttu-id="639fa-118">Eliminare qualsiasi attività in corso</span><span class="sxs-lookup"><span data-stu-id="639fa-118">Delete any running task</span></span>

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

### <span data-ttu-id="639fa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="639fa-119">-Force</span></span>
<span data-ttu-id="639fa-120">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="639fa-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="639fa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="639fa-121">-InputObject</span></span>
<span data-ttu-id="639fa-122">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="639fa-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="639fa-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="639fa-123">-Name</span></span>
<span data-ttu-id="639fa-124">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="639fa-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="639fa-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="639fa-125">-PassThru</span></span>
<span data-ttu-id="639fa-126">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="639fa-126">Returns an true/false.</span></span>
<span data-ttu-id="639fa-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="639fa-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="639fa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639fa-128">-ResourceGroupName</span></span>
<span data-ttu-id="639fa-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="639fa-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="639fa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="639fa-130">-ResourceId</span></span>
<span data-ttu-id="639fa-131">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="639fa-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="639fa-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="639fa-132">-Confirm</span></span>
<span data-ttu-id="639fa-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="639fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="639fa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="639fa-134">-WhatIf</span></span>
<span data-ttu-id="639fa-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="639fa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="639fa-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="639fa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="639fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639fa-137">CommonParameters</span></span>
<span data-ttu-id="639fa-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639fa-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="639fa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639fa-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="639fa-140">INPUTS</span></span>

### <span data-ttu-id="639fa-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="639fa-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="639fa-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="639fa-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="639fa-143">System. String</span><span class="sxs-lookup"><span data-stu-id="639fa-143">System.String</span></span>

## <span data-ttu-id="639fa-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="639fa-144">OUTPUTS</span></span>

### <span data-ttu-id="639fa-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="639fa-145">System.Boolean</span></span>

## <span data-ttu-id="639fa-146">Note</span><span class="sxs-lookup"><span data-stu-id="639fa-146">NOTES</span></span>

## <span data-ttu-id="639fa-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="639fa-147">RELATED LINKS</span></span>
