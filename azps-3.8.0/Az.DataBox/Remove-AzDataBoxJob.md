---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020122"
---
# <span data-ttu-id="6663a-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="6663a-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="6663a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6663a-102">SYNOPSIS</span></span>
<span data-ttu-id="6663a-103">Elimina il processo databox</span><span class="sxs-lookup"><span data-stu-id="6663a-103">Deletes the databox job</span></span>

## <span data-ttu-id="6663a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6663a-104">SYNTAX</span></span>

### <span data-ttu-id="6663a-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6663a-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6663a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6663a-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6663a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6663a-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6663a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6663a-108">DESCRIPTION</span></span>
<span data-ttu-id="6663a-109">Il cmdlet **Remove-AzDataBoxJob** viene usato per eliminare un processo databox finito dall'elenco dei processi di databox.</span><span class="sxs-lookup"><span data-stu-id="6663a-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="6663a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6663a-110">EXAMPLES</span></span>

### <span data-ttu-id="6663a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6663a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="6663a-112">Elimina il processo databox specificato</span><span class="sxs-lookup"><span data-stu-id="6663a-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="6663a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6663a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="6663a-114">Elimina il processo databox specificato con forza senza conferma</span><span class="sxs-lookup"><span data-stu-id="6663a-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="6663a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6663a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="6663a-116">Elimina il processo databox specificato</span><span class="sxs-lookup"><span data-stu-id="6663a-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="6663a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6663a-117">PARAMETERS</span></span>

### <span data-ttu-id="6663a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6663a-118">-DefaultProfile</span></span>
<span data-ttu-id="6663a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6663a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6663a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6663a-120">-Force</span></span>
<span data-ttu-id="6663a-121">Rimozione forzata senza conferma</span><span class="sxs-lookup"><span data-stu-id="6663a-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="6663a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6663a-122">-InputObject</span></span>
<span data-ttu-id="6663a-123">InputObject di tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="6663a-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="6663a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6663a-124">-Name</span></span>
<span data-ttu-id="6663a-125">Nome processo databox</span><span class="sxs-lookup"><span data-stu-id="6663a-125">Databox Job Name</span></span>

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

### <span data-ttu-id="6663a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6663a-126">-PassThru</span></span>
<span data-ttu-id="6663a-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="6663a-127">PassThru</span></span>

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

### <span data-ttu-id="6663a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6663a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6663a-129">Nome gruppo risorse processo databox</span><span class="sxs-lookup"><span data-stu-id="6663a-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="6663a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6663a-130">-ResourceId</span></span>
<span data-ttu-id="6663a-131">ID risorsa processo databox</span><span class="sxs-lookup"><span data-stu-id="6663a-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="6663a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6663a-132">-Confirm</span></span>
<span data-ttu-id="6663a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6663a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6663a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6663a-134">-WhatIf</span></span>
<span data-ttu-id="6663a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6663a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6663a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6663a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6663a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6663a-137">CommonParameters</span></span>
<span data-ttu-id="6663a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6663a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6663a-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6663a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6663a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6663a-140">INPUTS</span></span>

### <span data-ttu-id="6663a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6663a-141">System.String</span></span>

## <span data-ttu-id="6663a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6663a-142">OUTPUTS</span></span>

### <span data-ttu-id="6663a-143">System. void</span><span class="sxs-lookup"><span data-stu-id="6663a-143">System.Void</span></span>

## <span data-ttu-id="6663a-144">Note</span><span class="sxs-lookup"><span data-stu-id="6663a-144">NOTES</span></span>

## <span data-ttu-id="6663a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6663a-145">RELATED LINKS</span></span>
