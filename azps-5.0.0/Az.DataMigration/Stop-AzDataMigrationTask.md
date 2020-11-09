---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297582"
---
# <span data-ttu-id="c2332-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c2332-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="c2332-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2332-102">SYNOPSIS</span></span>
<span data-ttu-id="c2332-103">Interrompe un'attività del servizio di migrazione del database di Azure in uno stato in corso.</span><span class="sxs-lookup"><span data-stu-id="c2332-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="c2332-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2332-104">SYNTAX</span></span>

### <span data-ttu-id="c2332-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2332-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2332-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2332-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2332-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2332-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2332-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2332-108">DESCRIPTION</span></span>
<span data-ttu-id="c2332-109">Stop-AzDataMigrationTask cmdlet interrompe l'attività di migrazione del database in stato di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c2332-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="c2332-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2332-110">EXAMPLES</span></span>

### <span data-ttu-id="c2332-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2332-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="c2332-112">L'esempio precedente arresta l'attività del servizio di migrazione del database di Azure denominata myDMSTask associata all'istanza del servizio di migrazione del database di Project myDMSProject e Azure denominata TestService</span><span class="sxs-lookup"><span data-stu-id="c2332-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="c2332-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c2332-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="c2332-114">Sopra l'esempio arresta l'attività del servizio di migrazione del database Azure passata come oggetto PSProjectTask parametro di input</span><span class="sxs-lookup"><span data-stu-id="c2332-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="c2332-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2332-115">PARAMETERS</span></span>

### <span data-ttu-id="c2332-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2332-116">-DefaultProfile</span></span>
<span data-ttu-id="c2332-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2332-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2332-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2332-118">-InputObject</span></span>
<span data-ttu-id="c2332-119">Oggetto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="c2332-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="c2332-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2332-120">-Name</span></span>
<span data-ttu-id="c2332-121">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c2332-121">The name of the task.</span></span>

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

### <span data-ttu-id="c2332-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2332-122">-PassThru</span></span>
<span data-ttu-id="c2332-123">Restituisce un valore true/false.</span><span class="sxs-lookup"><span data-stu-id="c2332-123">Returns an true/false.</span></span>
<span data-ttu-id="c2332-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c2332-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2332-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c2332-125">-ProjectName</span></span>
<span data-ttu-id="c2332-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="c2332-126">The name of the project.</span></span>

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

### <span data-ttu-id="c2332-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2332-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2332-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2332-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="c2332-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2332-129">-ResourceId</span></span>
<span data-ttu-id="c2332-130">ID risorsa ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="c2332-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="c2332-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c2332-131">-ServiceName</span></span>
<span data-ttu-id="c2332-132">Nome del servizio di migrazione del database.</span><span class="sxs-lookup"><span data-stu-id="c2332-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c2332-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2332-133">-Confirm</span></span>
<span data-ttu-id="c2332-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2332-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2332-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2332-135">-WhatIf</span></span>
<span data-ttu-id="c2332-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2332-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2332-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2332-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2332-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2332-138">CommonParameters</span></span>
<span data-ttu-id="c2332-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2332-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2332-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2332-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2332-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2332-141">INPUTS</span></span>

### <span data-ttu-id="c2332-142">Microsoft. Azure. Commands. DataMigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c2332-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="c2332-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c2332-143">System.String</span></span>

## <span data-ttu-id="c2332-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2332-144">OUTPUTS</span></span>

### <span data-ttu-id="c2332-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2332-145">System.Boolean</span></span>

## <span data-ttu-id="c2332-146">Note</span><span class="sxs-lookup"><span data-stu-id="c2332-146">NOTES</span></span>

## <span data-ttu-id="c2332-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2332-147">RELATED LINKS</span></span>
