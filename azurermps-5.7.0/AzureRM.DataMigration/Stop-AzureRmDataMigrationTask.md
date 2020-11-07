---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686325"
---
# <span data-ttu-id="62223-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="62223-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="62223-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62223-102">SYNOPSIS</span></span>
<span data-ttu-id="62223-103">Interrompe un'attività del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="62223-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62223-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62223-104">SYNTAX</span></span>

### <span data-ttu-id="62223-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62223-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62223-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62223-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62223-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62223-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="62223-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62223-108">DESCRIPTION</span></span>
<span data-ttu-id="62223-109">Stop-AzureRmDataMigrationTask cmdlet interrompe l'attività di migrazione del database in stato di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="62223-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="62223-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62223-110">EXAMPLES</span></span>

### <span data-ttu-id="62223-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62223-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="62223-112">L'esempio precedente arresta l'attività del servizio di migrazione del database di Azure denominata myDMSTask associata all'istanza del servizio di migrazione del database di Project myDMSProject e Azure denominata TestService</span><span class="sxs-lookup"><span data-stu-id="62223-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="62223-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="62223-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="62223-114">Sopra l'esempio arresta l'attività del servizio di migrazione del database Azure passata come oggetto PSProjectTask parametro di input</span><span class="sxs-lookup"><span data-stu-id="62223-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="62223-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62223-115">PARAMETERS</span></span>

### <span data-ttu-id="62223-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62223-116">-Confirm</span></span>
<span data-ttu-id="62223-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62223-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62223-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62223-118">-DefaultProfile</span></span>
<span data-ttu-id="62223-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62223-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62223-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62223-120">-InputObject</span></span>
<span data-ttu-id="62223-121">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="62223-121">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62223-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="62223-122">-Name</span></span>
<span data-ttu-id="62223-123">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="62223-123">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62223-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62223-124">-PassThru</span></span>
<span data-ttu-id="62223-125">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="62223-125">Returns an true/false.</span></span>
<span data-ttu-id="62223-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="62223-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62223-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="62223-127">-ProjectName</span></span>
<span data-ttu-id="62223-128">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="62223-128">The name of the project.</span></span>

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

### <span data-ttu-id="62223-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62223-129">-ResourceGroupName</span></span>
<span data-ttu-id="62223-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62223-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="62223-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62223-131">-ResourceId</span></span>
<span data-ttu-id="62223-132">ID risorsa ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="62223-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="62223-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="62223-133">-ServiceName</span></span>
<span data-ttu-id="62223-134">Nome del servizio di migrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="62223-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="62223-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62223-135">-WhatIf</span></span>
<span data-ttu-id="62223-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62223-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62223-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62223-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="62223-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62223-138">INPUTS</span></span>

### <span data-ttu-id="62223-139">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="62223-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="62223-140">System. String</span><span class="sxs-lookup"><span data-stu-id="62223-140">System.String</span></span>


## <span data-ttu-id="62223-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62223-141">OUTPUTS</span></span>

### <span data-ttu-id="62223-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62223-142">System.Boolean</span></span>


## <span data-ttu-id="62223-143">Note</span><span class="sxs-lookup"><span data-stu-id="62223-143">NOTES</span></span>

## <span data-ttu-id="62223-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62223-144">RELATED LINKS</span></span>

