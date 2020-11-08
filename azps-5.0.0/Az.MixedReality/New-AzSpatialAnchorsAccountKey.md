---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200769"
---
# <span data-ttu-id="45142-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="45142-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="45142-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45142-102">SYNOPSIS</span></span>
<span data-ttu-id="45142-103">Chiave di rigenerazione dell'account degli ancoraggi spaziali</span><span class="sxs-lookup"><span data-stu-id="45142-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="45142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45142-104">SYNTAX</span></span>

### <span data-ttu-id="45142-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="45142-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45142-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="45142-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45142-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="45142-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45142-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="45142-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45142-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="45142-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45142-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="45142-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45142-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45142-111">DESCRIPTION</span></span>
<span data-ttu-id="45142-112">Rigenerare la chiave primaria o la chiave secondaria di un account di ancoraggio spaziale.</span><span class="sxs-lookup"><span data-stu-id="45142-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="45142-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45142-113">EXAMPLES</span></span>

### <span data-ttu-id="45142-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45142-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="45142-115">Rigenera chiave secondaria di un account di ancoraggio spaziale "esempio" nel gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="45142-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="45142-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="45142-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="45142-117">Rigenerazione della chiave secondaria dell'account degli ancoraggi spaziali "esempio" dal gruppo di risorse e dell'abbonamento corrente "RG1" con piping.</span><span class="sxs-lookup"><span data-stu-id="45142-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="45142-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45142-118">PARAMETERS</span></span>

### <span data-ttu-id="45142-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45142-119">-DefaultProfile</span></span>
<span data-ttu-id="45142-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45142-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45142-121">-Force</span><span class="sxs-lookup"><span data-stu-id="45142-121">-Force</span></span>
<span data-ttu-id="45142-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="45142-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45142-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45142-123">-InputObject</span></span>
<span data-ttu-id="45142-124">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="45142-124">The custom domain object.</span></span>

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

### <span data-ttu-id="45142-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="45142-125">-Name</span></span>
<span data-ttu-id="45142-126">Nome dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="45142-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="45142-127">-Primaria</span><span class="sxs-lookup"><span data-stu-id="45142-127">-Primary</span></span>
<span data-ttu-id="45142-128">Rigenerare la chiave primaria dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="45142-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="45142-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45142-129">-ResourceGroupName</span></span>
<span data-ttu-id="45142-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="45142-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="45142-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45142-131">-ResourceId</span></span>
<span data-ttu-id="45142-132">ID risorsa dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="45142-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="45142-133">-Secondario</span><span class="sxs-lookup"><span data-stu-id="45142-133">-Secondary</span></span>
<span data-ttu-id="45142-134">Rigenerare la chiave primaria dell'account degli ancoraggi spaziali.</span><span class="sxs-lookup"><span data-stu-id="45142-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="45142-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45142-135">-Confirm</span></span>
<span data-ttu-id="45142-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45142-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45142-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45142-137">-WhatIf</span></span>
<span data-ttu-id="45142-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45142-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45142-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45142-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45142-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45142-140">CommonParameters</span></span>
<span data-ttu-id="45142-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45142-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="45142-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45142-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45142-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45142-143">INPUTS</span></span>

### <span data-ttu-id="45142-144">System. String</span><span class="sxs-lookup"><span data-stu-id="45142-144">System.String</span></span>

### <span data-ttu-id="45142-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="45142-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="45142-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45142-146">OUTPUTS</span></span>

### <span data-ttu-id="45142-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="45142-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="45142-148">Note</span><span class="sxs-lookup"><span data-stu-id="45142-148">NOTES</span></span>

## <span data-ttu-id="45142-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45142-149">RELATED LINKS</span></span>
