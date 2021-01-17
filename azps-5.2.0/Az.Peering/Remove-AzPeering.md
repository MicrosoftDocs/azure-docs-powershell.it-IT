---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331723"
---
# <span data-ttu-id="c6cba-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c6cba-101">Remove-AzPeering</span></span>

## <span data-ttu-id="c6cba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6cba-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cba-103">Eliminare o rimuovere un peering.</span><span class="sxs-lookup"><span data-stu-id="c6cba-103">Delete or remove a peering.</span></span> <span data-ttu-id="c6cba-104">Questo eliminerà tutte le risorse figlio o gli avvisi sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="c6cba-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="c6cba-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6cba-105">SYNTAX</span></span>

### <span data-ttu-id="c6cba-106">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6cba-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6cba-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c6cba-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6cba-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6cba-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6cba-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6cba-109">DESCRIPTION</span></span>
<span data-ttu-id="c6cba-110">Perminently eliminare una risorsa peering.</span><span class="sxs-lookup"><span data-stu-id="c6cba-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="c6cba-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6cba-111">EXAMPLES</span></span>

### <span data-ttu-id="c6cba-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6cba-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="c6cba-113">Rimuovere un peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c6cba-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="c6cba-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6cba-114">PARAMETERS</span></span>

### <span data-ttu-id="c6cba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6cba-115">-AsJob</span></span>
<span data-ttu-id="c6cba-116">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="c6cba-116">Run in the background.</span></span>

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

### <span data-ttu-id="c6cba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6cba-117">-DefaultProfile</span></span>
<span data-ttu-id="c6cba-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6cba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6cba-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c6cba-119">-Force</span></span>
<span data-ttu-id="c6cba-120">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="c6cba-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="c6cba-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6cba-121">-InputObject</span></span>
<span data-ttu-id="c6cba-122">USA Get-AzPeering per recuperare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6cba-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6cba-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6cba-123">-Name</span></span>
<span data-ttu-id="c6cba-124">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c6cba-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cba-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6cba-125">-PassThru</span></span>
<span data-ttu-id="c6cba-126">Restituisce vero se completo</span><span class="sxs-lookup"><span data-stu-id="c6cba-126">Return true if complete</span></span>

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

### <span data-ttu-id="c6cba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6cba-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6cba-128">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="c6cba-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cba-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6cba-129">-ResourceId</span></span>
<span data-ttu-id="c6cba-130">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c6cba-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6cba-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6cba-131">-Confirm</span></span>
<span data-ttu-id="c6cba-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6cba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6cba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6cba-133">-WhatIf</span></span>
<span data-ttu-id="c6cba-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6cba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6cba-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6cba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6cba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6cba-136">CommonParameters</span></span>
<span data-ttu-id="c6cba-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6cba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6cba-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6cba-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6cba-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6cba-139">INPUTS</span></span>

### <span data-ttu-id="c6cba-140">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c6cba-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c6cba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c6cba-141">System.String</span></span>

## <span data-ttu-id="c6cba-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6cba-142">OUTPUTS</span></span>

### <span data-ttu-id="c6cba-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6cba-143">System.Boolean</span></span>

## <span data-ttu-id="c6cba-144">Note</span><span class="sxs-lookup"><span data-stu-id="c6cba-144">NOTES</span></span>

## <span data-ttu-id="c6cba-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6cba-145">RELATED LINKS</span></span>
