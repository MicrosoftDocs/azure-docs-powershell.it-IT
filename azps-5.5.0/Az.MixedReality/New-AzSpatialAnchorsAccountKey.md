---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185015"
---
# <span data-ttu-id="c7032-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c7032-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="c7032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7032-102">SYNOPSIS</span></span>
<span data-ttu-id="c7032-103">Rigenerare la chiave dell'account degli ancoraggi nello stato spaziale</span><span class="sxs-lookup"><span data-stu-id="c7032-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="c7032-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7032-104">SYNTAX</span></span>

### <span data-ttu-id="c7032-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7032-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7032-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7032-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7032-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7032-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7032-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7032-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7032-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7032-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7032-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7032-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7032-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7032-111">DESCRIPTION</span></span>
<span data-ttu-id="c7032-112">Rigenerare la chiave primaria o la chiave secondaria dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="c7032-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="c7032-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7032-113">EXAMPLES</span></span>

### <span data-ttu-id="c7032-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7032-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="c7032-115">Rigenerare la chiave secondaria dell'account degli ancoraggi nello stato "example" nel gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="c7032-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="c7032-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c7032-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c7032-117">Rigenerare la chiave secondaria dell'account degli ancoraggi nello spaziale "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="c7032-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="c7032-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7032-118">PARAMETERS</span></span>

### <span data-ttu-id="c7032-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7032-119">-DefaultProfile</span></span>
<span data-ttu-id="c7032-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7032-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c7032-121">-Force</span></span>
<span data-ttu-id="c7032-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="c7032-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7032-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7032-123">-InputObject</span></span>
<span data-ttu-id="c7032-124">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c7032-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c7032-125">-Name</span></span>
<span data-ttu-id="c7032-126">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="c7032-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-127">-Principale</span><span class="sxs-lookup"><span data-stu-id="c7032-127">-Primary</span></span>
<span data-ttu-id="c7032-128">Rigenerare la chiave primaria dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="c7032-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7032-129">-ResourceGroupName</span></span>
<span data-ttu-id="c7032-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7032-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7032-131">-ResourceId</span></span>
<span data-ttu-id="c7032-132">ID risorsa dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="c7032-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="c7032-133">-Secondary</span></span>
<span data-ttu-id="c7032-134">Rigenerare la chiave primaria dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="c7032-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7032-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7032-135">-Confirm</span></span>
<span data-ttu-id="c7032-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7032-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7032-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7032-137">-WhatIf</span></span>
<span data-ttu-id="c7032-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7032-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7032-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7032-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7032-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7032-140">CommonParameters</span></span>
<span data-ttu-id="c7032-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7032-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c7032-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7032-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7032-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7032-143">INPUTS</span></span>

### <span data-ttu-id="c7032-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c7032-144">System.String</span></span>

### <span data-ttu-id="c7032-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c7032-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c7032-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7032-146">OUTPUTS</span></span>

### <span data-ttu-id="c7032-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c7032-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="c7032-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7032-148">NOTES</span></span>

## <span data-ttu-id="c7032-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7032-149">RELATED LINKS</span></span>
