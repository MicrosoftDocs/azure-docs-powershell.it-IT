---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: ba6817928751c67e87f6641a6362a1fbf84eece8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989321"
---
# <span data-ttu-id="84c8d-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="84c8d-101">Remove-AzPeering</span></span>

## <span data-ttu-id="84c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="84c8d-103">Eliminare o rimuovere un peering.</span><span class="sxs-lookup"><span data-stu-id="84c8d-103">Delete or remove a peering.</span></span> <span data-ttu-id="84c8d-104">Verranno eliminate tutte le risorse figlio o verrà visualizzato un avviso sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="84c8d-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="84c8d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84c8d-105">SYNTAX</span></span>

### <span data-ttu-id="84c8d-106">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84c8d-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84c8d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="84c8d-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84c8d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84c8d-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c8d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84c8d-109">DESCRIPTION</span></span>
<span data-ttu-id="84c8d-110">Eliminare in modo minuta una risorsa di peering.</span><span class="sxs-lookup"><span data-stu-id="84c8d-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="84c8d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84c8d-111">EXAMPLES</span></span>

### <span data-ttu-id="84c8d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84c8d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="84c8d-113">Rimuovere un peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="84c8d-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="84c8d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84c8d-114">PARAMETERS</span></span>

### <span data-ttu-id="84c8d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84c8d-115">-AsJob</span></span>
<span data-ttu-id="84c8d-116">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="84c8d-116">Run in the background.</span></span>

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

### <span data-ttu-id="84c8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c8d-117">-DefaultProfile</span></span>
<span data-ttu-id="84c8d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84c8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c8d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84c8d-119">-Force</span></span>
<span data-ttu-id="84c8d-120">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="84c8d-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="84c8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84c8d-121">-InputObject</span></span>
<span data-ttu-id="84c8d-122">Usare Get-AzPeering per recuperare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84c8d-122">Use Get-AzPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="84c8d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="84c8d-123">-Name</span></span>
<span data-ttu-id="84c8d-124">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="84c8d-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="84c8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84c8d-125">-PassThru</span></span>
<span data-ttu-id="84c8d-126">Return true if complete</span><span class="sxs-lookup"><span data-stu-id="84c8d-126">Return true if complete</span></span>

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

### <span data-ttu-id="84c8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="84c8d-128">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="84c8d-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="84c8d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84c8d-129">-ResourceId</span></span>
<span data-ttu-id="84c8d-130">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="84c8d-130">The resource id string name.</span></span>

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

### <span data-ttu-id="84c8d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84c8d-131">-Confirm</span></span>
<span data-ttu-id="84c8d-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c8d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c8d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c8d-133">-WhatIf</span></span>
<span data-ttu-id="84c8d-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84c8d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c8d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84c8d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c8d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c8d-136">CommonParameters</span></span>
<span data-ttu-id="84c8d-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c8d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c8d-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84c8d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c8d-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="84c8d-139">INPUTS</span></span>

### <span data-ttu-id="84c8d-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="84c8d-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="84c8d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="84c8d-141">System.String</span></span>

## <span data-ttu-id="84c8d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84c8d-142">OUTPUTS</span></span>

### <span data-ttu-id="84c8d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84c8d-143">System.Boolean</span></span>

## <span data-ttu-id="84c8d-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="84c8d-144">NOTES</span></span>

## <span data-ttu-id="84c8d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84c8d-145">RELATED LINKS</span></span>
