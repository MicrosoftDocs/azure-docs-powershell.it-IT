---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188670"
---
# <span data-ttu-id="e107a-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="e107a-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="e107a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e107a-102">SYNOPSIS</span></span>
<span data-ttu-id="e107a-103">Annulla un processo della casella dati in corso se il processo è in stato di annullamento.</span><span class="sxs-lookup"><span data-stu-id="e107a-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="e107a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e107a-104">SYNTAX</span></span>

### <span data-ttu-id="e107a-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e107a-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e107a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e107a-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e107a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e107a-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e107a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e107a-108">DESCRIPTION</span></span>
<span data-ttu-id="e107a-109">Il cmdlet **Stop-AzDataBoxJob** viene usato per annullare un processo di databox.</span><span class="sxs-lookup"><span data-stu-id="e107a-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="e107a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e107a-110">EXAMPLES</span></span>

### <span data-ttu-id="e107a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e107a-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="e107a-112">Annulla il processo specificato nella casella dati</span><span class="sxs-lookup"><span data-stu-id="e107a-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="e107a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e107a-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="e107a-114">Annulla il processo specificato in modo forzato senza conferma</span><span class="sxs-lookup"><span data-stu-id="e107a-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="e107a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e107a-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="e107a-116">Annulla il processo specificato nella casella dati</span><span class="sxs-lookup"><span data-stu-id="e107a-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="e107a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e107a-117">PARAMETERS</span></span>

### <span data-ttu-id="e107a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e107a-118">-DefaultProfile</span></span>
<span data-ttu-id="e107a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e107a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e107a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e107a-120">-Force</span></span>
<span data-ttu-id="e107a-121">Forzare l'arresto senza conferma</span><span class="sxs-lookup"><span data-stu-id="e107a-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="e107a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e107a-122">-InputObject</span></span>
<span data-ttu-id="e107a-123">InputObject di tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="e107a-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e107a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e107a-124">-Name</span></span>
<span data-ttu-id="e107a-125">Nome processo casella di dati</span><span class="sxs-lookup"><span data-stu-id="e107a-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e107a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e107a-126">-PassThru</span></span>
<span data-ttu-id="e107a-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="e107a-127">PassThru</span></span>

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

### <span data-ttu-id="e107a-128">-Motivo</span><span class="sxs-lookup"><span data-stu-id="e107a-128">-Reason</span></span>
<span data-ttu-id="e107a-129">Motivo dell'annullamento</span><span class="sxs-lookup"><span data-stu-id="e107a-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e107a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e107a-130">-ResourceGroupName</span></span>
<span data-ttu-id="e107a-131">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="e107a-131">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e107a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e107a-132">-ResourceId</span></span>
<span data-ttu-id="e107a-133">ID risorsa casella dati</span><span class="sxs-lookup"><span data-stu-id="e107a-133">Databox Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e107a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e107a-134">-Confirm</span></span>
<span data-ttu-id="e107a-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e107a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e107a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e107a-136">-WhatIf</span></span>
<span data-ttu-id="e107a-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e107a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e107a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e107a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e107a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e107a-139">CommonParameters</span></span>
<span data-ttu-id="e107a-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e107a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e107a-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e107a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e107a-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="e107a-142">INPUTS</span></span>

### <span data-ttu-id="e107a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e107a-143">System.String</span></span>

## <span data-ttu-id="e107a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e107a-144">OUTPUTS</span></span>

### <span data-ttu-id="e107a-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="e107a-145">System.Void</span></span>

## <span data-ttu-id="e107a-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="e107a-146">NOTES</span></span>

## <span data-ttu-id="e107a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e107a-147">RELATED LINKS</span></span>
