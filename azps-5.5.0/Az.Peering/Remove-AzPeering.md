---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202255"
---
# <span data-ttu-id="90ff7-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="90ff7-101">Remove-AzPeering</span></span>

## <span data-ttu-id="90ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="90ff7-103">Eliminare o rimuovere un peering.</span><span class="sxs-lookup"><span data-stu-id="90ff7-103">Delete or remove a peering.</span></span> <span data-ttu-id="90ff7-104">Verranno eliminate tutte le risorse figlio o verrà visualizzato un avviso sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="90ff7-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="90ff7-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90ff7-105">SYNTAX</span></span>

### <span data-ttu-id="90ff7-106">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90ff7-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="90ff7-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff7-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="90ff7-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90ff7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="90ff7-109">DESCRIPTION</span></span>
<span data-ttu-id="90ff7-110">Eliminare in modo minuta una risorsa di peering.</span><span class="sxs-lookup"><span data-stu-id="90ff7-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="90ff7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90ff7-111">EXAMPLES</span></span>

### <span data-ttu-id="90ff7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90ff7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="90ff7-113">Rimuovere un peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="90ff7-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="90ff7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90ff7-114">PARAMETERS</span></span>

### <span data-ttu-id="90ff7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90ff7-115">-AsJob</span></span>
<span data-ttu-id="90ff7-116">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="90ff7-116">Run in the background.</span></span>

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

### <span data-ttu-id="90ff7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ff7-117">-DefaultProfile</span></span>
<span data-ttu-id="90ff7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90ff7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ff7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="90ff7-119">-Force</span></span>
<span data-ttu-id="90ff7-120">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="90ff7-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="90ff7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90ff7-121">-InputObject</span></span>
<span data-ttu-id="90ff7-122">Usare Get-AzPeering per recuperare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="90ff7-122">Use Get-AzPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="90ff7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="90ff7-123">-Name</span></span>
<span data-ttu-id="90ff7-124">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="90ff7-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="90ff7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90ff7-125">-PassThru</span></span>
<span data-ttu-id="90ff7-126">Return true if complete</span><span class="sxs-lookup"><span data-stu-id="90ff7-126">Return true if complete</span></span>

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

### <span data-ttu-id="90ff7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ff7-127">-ResourceGroupName</span></span>
<span data-ttu-id="90ff7-128">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="90ff7-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="90ff7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90ff7-129">-ResourceId</span></span>
<span data-ttu-id="90ff7-130">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="90ff7-130">The resource id string name.</span></span>

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

### <span data-ttu-id="90ff7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90ff7-131">-Confirm</span></span>
<span data-ttu-id="90ff7-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ff7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ff7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ff7-133">-WhatIf</span></span>
<span data-ttu-id="90ff7-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ff7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ff7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ff7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ff7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ff7-136">CommonParameters</span></span>
<span data-ttu-id="90ff7-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ff7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ff7-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90ff7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ff7-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="90ff7-139">INPUTS</span></span>

### <span data-ttu-id="90ff7-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSApplicationing</span><span class="sxs-lookup"><span data-stu-id="90ff7-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="90ff7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="90ff7-141">System.String</span></span>

## <span data-ttu-id="90ff7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90ff7-142">OUTPUTS</span></span>

### <span data-ttu-id="90ff7-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90ff7-143">System.Boolean</span></span>

## <span data-ttu-id="90ff7-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="90ff7-144">NOTES</span></span>

## <span data-ttu-id="90ff7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90ff7-145">RELATED LINKS</span></span>
