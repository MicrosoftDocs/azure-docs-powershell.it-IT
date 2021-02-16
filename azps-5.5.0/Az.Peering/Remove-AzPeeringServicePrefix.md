---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184023"
---
# <span data-ttu-id="b904e-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b904e-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="b904e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b904e-102">SYNOPSIS</span></span>
<span data-ttu-id="b904e-103">Rimuove un nuovo prefisso del servizio di peering</span><span class="sxs-lookup"><span data-stu-id="b904e-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="b904e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b904e-104">SYNTAX</span></span>

### <span data-ttu-id="b904e-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b904e-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b904e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b904e-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b904e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b904e-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b904e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b904e-108">DESCRIPTION</span></span>
<span data-ttu-id="b904e-109">Rimuove un prefisso del servizio di peering da un servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="b904e-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="b904e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b904e-110">EXAMPLES</span></span>

### <span data-ttu-id="b904e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b904e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="b904e-112">Rimuovere un prefisso da un oggetto servizio di peering</span><span class="sxs-lookup"><span data-stu-id="b904e-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="b904e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b904e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="b904e-114">Rimuovere un prefisso da un ID di risorsa del servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="b904e-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="b904e-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b904e-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="b904e-116">Rimuovere un prefisso dal nome e dal nome di un gruppo di risorse del servizio di peering</span><span class="sxs-lookup"><span data-stu-id="b904e-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="b904e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b904e-117">PARAMETERS</span></span>

### <span data-ttu-id="b904e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b904e-118">-AsJob</span></span>
<span data-ttu-id="b904e-119">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="b904e-119">Run in the background.</span></span>

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

### <span data-ttu-id="b904e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b904e-120">-DefaultProfile</span></span>
<span data-ttu-id="b904e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b904e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b904e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b904e-122">-Force</span></span>
<span data-ttu-id="b904e-123">Forzare il completamento dell'operazione</span><span class="sxs-lookup"><span data-stu-id="b904e-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="b904e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b904e-124">-InputObject</span></span>
<span data-ttu-id="b904e-125">Usare un Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b904e-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b904e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b904e-126">-Name</span></span>
<span data-ttu-id="b904e-127">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="b904e-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b904e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b904e-128">-PassThru</span></span>
<span data-ttu-id="b904e-129">Restituisce true per success o false per failed.</span><span class="sxs-lookup"><span data-stu-id="b904e-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="b904e-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="b904e-130">-PrefixName</span></span>
<span data-ttu-id="b904e-131">Nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="b904e-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b904e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b904e-132">-ResourceGroupName</span></span>
<span data-ttu-id="b904e-133">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b904e-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b904e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b904e-134">-ResourceId</span></span>
<span data-ttu-id="b904e-135">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b904e-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b904e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b904e-136">-Confirm</span></span>
<span data-ttu-id="b904e-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b904e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b904e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b904e-138">-WhatIf</span></span>
<span data-ttu-id="b904e-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b904e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b904e-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b904e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b904e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b904e-141">CommonParameters</span></span>
<span data-ttu-id="b904e-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b904e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b904e-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b904e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b904e-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="b904e-144">INPUTS</span></span>

### <span data-ttu-id="b904e-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPreingServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b904e-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="b904e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b904e-146">System.String</span></span>

## <span data-ttu-id="b904e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b904e-147">OUTPUTS</span></span>

### <span data-ttu-id="b904e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b904e-148">System.Boolean</span></span>

## <span data-ttu-id="b904e-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="b904e-149">NOTES</span></span>

## <span data-ttu-id="b904e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b904e-150">RELATED LINKS</span></span>
