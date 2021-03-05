---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965214"
---
# <span data-ttu-id="579d4-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="579d4-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="579d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="579d4-102">SYNOPSIS</span></span>
<span data-ttu-id="579d4-103">Elimina una attestazione.</span><span class="sxs-lookup"><span data-stu-id="579d4-103">Deletes an attestation.</span></span>

## <span data-ttu-id="579d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="579d4-104">SYNTAX</span></span>

### <span data-ttu-id="579d4-105">ByAvailableAttestation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="579d4-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="579d4-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="579d4-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="579d4-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="579d4-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="579d4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="579d4-108">DESCRIPTION</span></span>
<span data-ttu-id="579d4-109">Il Remove-AzAttestation cmdlet elimina la attestazione specificata.</span><span class="sxs-lookup"><span data-stu-id="579d4-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="579d4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="579d4-110">EXAMPLES</span></span>

### <span data-ttu-id="579d4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="579d4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="579d4-112">Eliminare il provider di attestazione *denominato pshtest3* nel gruppo di risorse *denominato psh-test-rg* dalla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="579d4-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="579d4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="579d4-113">PARAMETERS</span></span>

### <span data-ttu-id="579d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579d4-114">-DefaultProfile</span></span>
<span data-ttu-id="579d4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="579d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="579d4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="579d4-116">-InputObject</span></span>
<span data-ttu-id="579d4-117">Oggetto di attestazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="579d4-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="579d4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="579d4-118">-Name</span></span>
<span data-ttu-id="579d4-119">Specifica il nome della attestazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="579d4-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579d4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="579d4-120">-PassThru</span></span>
<span data-ttu-id="579d4-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="579d4-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="579d4-122">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="579d4-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="579d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="579d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="579d4-124">Specifica il nome del gruppo di risorse per l'attestazione di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="579d4-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579d4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="579d4-125">-ResourceId</span></span>
<span data-ttu-id="579d4-126">ID risorsa attestazione.</span><span class="sxs-lookup"><span data-stu-id="579d4-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579d4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="579d4-127">-Confirm</span></span>
<span data-ttu-id="579d4-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="579d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="579d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="579d4-129">-WhatIf</span></span>
<span data-ttu-id="579d4-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="579d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="579d4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="579d4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="579d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579d4-132">CommonParameters</span></span>
<span data-ttu-id="579d4-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579d4-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="579d4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579d4-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="579d4-135">INPUTS</span></span>

### <span data-ttu-id="579d4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="579d4-136">System.String</span></span>

### <span data-ttu-id="579d4-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="579d4-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="579d4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="579d4-138">OUTPUTS</span></span>

### <span data-ttu-id="579d4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="579d4-139">System.Boolean</span></span>

## <span data-ttu-id="579d4-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="579d4-140">NOTES</span></span>

## <span data-ttu-id="579d4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="579d4-141">RELATED LINKS</span></span>
