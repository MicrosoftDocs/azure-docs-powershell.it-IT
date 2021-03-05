---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 7c94b9fd1395af8b64425837d1fb08c578b3c2a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010461"
---
# <span data-ttu-id="91cb0-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="91cb0-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="91cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="91cb0-103">Rigenerare la chiave dell'account degli ancoraggi nello stato spaziale</span><span class="sxs-lookup"><span data-stu-id="91cb0-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="91cb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91cb0-104">SYNTAX</span></span>

### <span data-ttu-id="91cb0-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cb0-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cb0-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cb0-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cb0-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cb0-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cb0-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cb0-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cb0-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cb0-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cb0-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cb0-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91cb0-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91cb0-111">DESCRIPTION</span></span>
<span data-ttu-id="91cb0-112">Rigenerare la chiave primaria o la chiave secondaria dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="91cb0-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="91cb0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91cb0-113">EXAMPLES</span></span>

### <span data-ttu-id="91cb0-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91cb0-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="91cb0-115">Rigenerare la chiave secondaria dell'account degli ancoraggi nello stato "example" nel gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="91cb0-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="91cb0-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="91cb0-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="91cb0-117">Rigenerare la chiave secondaria dell'account degli ancoraggi nello spaziale "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="91cb0-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="91cb0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91cb0-118">PARAMETERS</span></span>

### <span data-ttu-id="91cb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cb0-119">-DefaultProfile</span></span>
<span data-ttu-id="91cb0-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91cb0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91cb0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="91cb0-121">-Force</span></span>
<span data-ttu-id="91cb0-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="91cb0-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91cb0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91cb0-123">-InputObject</span></span>
<span data-ttu-id="91cb0-124">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="91cb0-124">The custom domain object.</span></span>

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

### <span data-ttu-id="91cb0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91cb0-125">-Name</span></span>
<span data-ttu-id="91cb0-126">Nome account per gli ancoraggi nello spaziale.</span><span class="sxs-lookup"><span data-stu-id="91cb0-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="91cb0-127">-Principale</span><span class="sxs-lookup"><span data-stu-id="91cb0-127">-Primary</span></span>
<span data-ttu-id="91cb0-128">Rigenerare la chiave primaria dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="91cb0-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="91cb0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cb0-129">-ResourceGroupName</span></span>
<span data-ttu-id="91cb0-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="91cb0-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="91cb0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91cb0-131">-ResourceId</span></span>
<span data-ttu-id="91cb0-132">ID risorsa dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="91cb0-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="91cb0-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="91cb0-133">-Secondary</span></span>
<span data-ttu-id="91cb0-134">Rigenerare la chiave primaria dell'account degli ancoraggi nello stato spaziale.</span><span class="sxs-lookup"><span data-stu-id="91cb0-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="91cb0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91cb0-135">-Confirm</span></span>
<span data-ttu-id="91cb0-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91cb0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91cb0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91cb0-137">-WhatIf</span></span>
<span data-ttu-id="91cb0-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91cb0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91cb0-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91cb0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91cb0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cb0-140">CommonParameters</span></span>
<span data-ttu-id="91cb0-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91cb0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="91cb0-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cb0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cb0-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="91cb0-143">INPUTS</span></span>

### <span data-ttu-id="91cb0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="91cb0-144">System.String</span></span>

### <span data-ttu-id="91cb0-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="91cb0-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="91cb0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91cb0-146">OUTPUTS</span></span>

### <span data-ttu-id="91cb0-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="91cb0-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="91cb0-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="91cb0-148">NOTES</span></span>

## <span data-ttu-id="91cb0-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91cb0-149">RELATED LINKS</span></span>
