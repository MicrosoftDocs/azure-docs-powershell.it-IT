---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: aec7870522d5d25887c9cb7437a4a232d3021a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518687"
---
# <span data-ttu-id="1bff2-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="1bff2-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="1bff2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bff2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bff2-103">Interrompe un'attività del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="1bff2-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bff2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bff2-104">SYNTAX</span></span>

### <span data-ttu-id="1bff2-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1bff2-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bff2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bff2-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bff2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bff2-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bff2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bff2-108">DESCRIPTION</span></span>
<span data-ttu-id="1bff2-109">Stop-AzureRmDataMigrationTask cmdlet interrompe l'attività di migrazione del database in stato di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="1bff2-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="1bff2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bff2-110">EXAMPLES</span></span>

### <span data-ttu-id="1bff2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1bff2-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="1bff2-112">L'esempio precedente arresta l'attività del servizio di migrazione del database di Azure denominata myDMSTask associata all'istanza del servizio di migrazione del database di Project myDMSProject e Azure denominata TestService</span><span class="sxs-lookup"><span data-stu-id="1bff2-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="1bff2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1bff2-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="1bff2-114">Sopra l'esempio arresta l'attività del servizio di migrazione del database Azure passata come oggetto PSProjectTask parametro di input</span><span class="sxs-lookup"><span data-stu-id="1bff2-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="1bff2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bff2-115">PARAMETERS</span></span>

### <span data-ttu-id="1bff2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bff2-116">-DefaultProfile</span></span>
<span data-ttu-id="1bff2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bff2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bff2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bff2-118">-InputObject</span></span>
<span data-ttu-id="1bff2-119">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="1bff2-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="1bff2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bff2-120">-Name</span></span>
<span data-ttu-id="1bff2-121">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1bff2-121">The name of the task.</span></span>

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

### <span data-ttu-id="1bff2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bff2-122">-PassThru</span></span>
<span data-ttu-id="1bff2-123">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="1bff2-123">Returns an true/false.</span></span>
<span data-ttu-id="1bff2-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1bff2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1bff2-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1bff2-125">-ProjectName</span></span>
<span data-ttu-id="1bff2-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="1bff2-126">The name of the project.</span></span>

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

### <span data-ttu-id="1bff2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bff2-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bff2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1bff2-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="1bff2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bff2-129">-ResourceId</span></span>
<span data-ttu-id="1bff2-130">ID risorsa ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="1bff2-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="1bff2-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1bff2-131">-ServiceName</span></span>
<span data-ttu-id="1bff2-132">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="1bff2-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="1bff2-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bff2-133">-Confirm</span></span>
<span data-ttu-id="1bff2-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bff2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bff2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bff2-135">-WhatIf</span></span>
<span data-ttu-id="1bff2-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bff2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bff2-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bff2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bff2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bff2-138">CommonParameters</span></span>
<span data-ttu-id="1bff2-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bff2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bff2-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bff2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bff2-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bff2-141">INPUTS</span></span>

### <span data-ttu-id="1bff2-142">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="1bff2-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="1bff2-143">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1bff2-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1bff2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1bff2-144">System.String</span></span>

## <span data-ttu-id="1bff2-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bff2-145">OUTPUTS</span></span>

### <span data-ttu-id="1bff2-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bff2-146">System.Boolean</span></span>

## <span data-ttu-id="1bff2-147">Note</span><span class="sxs-lookup"><span data-stu-id="1bff2-147">NOTES</span></span>

## <span data-ttu-id="1bff2-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bff2-148">RELATED LINKS</span></span>
