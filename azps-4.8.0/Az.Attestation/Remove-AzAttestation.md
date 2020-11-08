---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033553"
---
# <span data-ttu-id="2713d-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="2713d-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="2713d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2713d-102">SYNOPSIS</span></span>
<span data-ttu-id="2713d-103">Elimina un'attestazione.</span><span class="sxs-lookup"><span data-stu-id="2713d-103">Deletes an attestation.</span></span>

## <span data-ttu-id="2713d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2713d-104">SYNTAX</span></span>

### <span data-ttu-id="2713d-105">ByAvailableAttestation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2713d-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2713d-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="2713d-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2713d-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="2713d-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2713d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2713d-108">DESCRIPTION</span></span>
<span data-ttu-id="2713d-109">Il cmdlet Remove-AzAttestation Elimina l'attestazione specificata.</span><span class="sxs-lookup"><span data-stu-id="2713d-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="2713d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2713d-110">EXAMPLES</span></span>

### <span data-ttu-id="2713d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2713d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="2713d-112">Eliminare il provider di attestazione denominato *pshtest3* nel gruppo risorse denominato *PSH-test-RG* dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="2713d-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="2713d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2713d-113">PARAMETERS</span></span>

### <span data-ttu-id="2713d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2713d-114">-DefaultProfile</span></span>
<span data-ttu-id="2713d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2713d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2713d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2713d-116">-InputObject</span></span>
<span data-ttu-id="2713d-117">Oggetto di attestazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2713d-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="2713d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2713d-118">-Name</span></span>
<span data-ttu-id="2713d-119">Specifica il nome dell'attestazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2713d-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="2713d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2713d-120">-PassThru</span></span>
<span data-ttu-id="2713d-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2713d-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2713d-122">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="2713d-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2713d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2713d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2713d-124">Specifica il nome del gruppo di risorse per l'attestazione di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2713d-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="2713d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2713d-125">-ResourceId</span></span>
<span data-ttu-id="2713d-126">ID risorsa attestazione.</span><span class="sxs-lookup"><span data-stu-id="2713d-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="2713d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2713d-127">-Confirm</span></span>
<span data-ttu-id="2713d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2713d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2713d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2713d-129">-WhatIf</span></span>
<span data-ttu-id="2713d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2713d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2713d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2713d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2713d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2713d-132">CommonParameters</span></span>
<span data-ttu-id="2713d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2713d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2713d-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2713d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2713d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2713d-135">INPUTS</span></span>

### <span data-ttu-id="2713d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2713d-136">System.String</span></span>

### <span data-ttu-id="2713d-137">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="2713d-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="2713d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2713d-138">OUTPUTS</span></span>

### <span data-ttu-id="2713d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2713d-139">System.Boolean</span></span>

## <span data-ttu-id="2713d-140">Note</span><span class="sxs-lookup"><span data-stu-id="2713d-140">NOTES</span></span>

## <span data-ttu-id="2713d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2713d-141">RELATED LINKS</span></span>
