---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675840"
---
# <span data-ttu-id="1771a-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="1771a-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="1771a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1771a-102">SYNOPSIS</span></span>
<span data-ttu-id="1771a-103">Elimina un'attestazione.</span><span class="sxs-lookup"><span data-stu-id="1771a-103">Deletes an attestation.</span></span>

## <span data-ttu-id="1771a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1771a-104">SYNTAX</span></span>

### <span data-ttu-id="1771a-105">ByAvailableAttestation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1771a-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1771a-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="1771a-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1771a-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="1771a-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1771a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1771a-108">DESCRIPTION</span></span>
<span data-ttu-id="1771a-109">Il cmdlet Remove-AzAttestation Elimina l'attestazione specificata.</span><span class="sxs-lookup"><span data-stu-id="1771a-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="1771a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1771a-110">EXAMPLES</span></span>

### <span data-ttu-id="1771a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1771a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="1771a-112">Eliminare l'attestazione "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="1771a-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="1771a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1771a-113">PARAMETERS</span></span>

### <span data-ttu-id="1771a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1771a-114">-AsJob</span></span>
<span data-ttu-id="1771a-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1771a-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1771a-116">-DefaultProfile</span></span>
<span data-ttu-id="1771a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1771a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1771a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1771a-118">-InputObject</span></span>
<span data-ttu-id="1771a-119">Oggetto di attestazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1771a-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1771a-120">-Name</span></span>
<span data-ttu-id="1771a-121">Specifica il nome dell'attestazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1771a-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1771a-122">-PassThru</span></span>
<span data-ttu-id="1771a-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1771a-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1771a-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="1771a-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1771a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1771a-126">Specifica il nome del gruppo di risorse per l'attestazione di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1771a-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1771a-127">-ResourceId</span></span>
<span data-ttu-id="1771a-128">ID risorsa attestazione.</span><span class="sxs-lookup"><span data-stu-id="1771a-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1771a-129">-Confirm</span></span>
<span data-ttu-id="1771a-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1771a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1771a-131">-WhatIf</span></span>
<span data-ttu-id="1771a-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1771a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1771a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1771a-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1771a-134">CommonParameters</span></span>
<span data-ttu-id="1771a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1771a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1771a-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1771a-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1771a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1771a-137">INPUTS</span></span>

### <span data-ttu-id="1771a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1771a-138">System.String</span></span>

### <span data-ttu-id="1771a-139">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="1771a-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="1771a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1771a-140">OUTPUTS</span></span>

### <span data-ttu-id="1771a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1771a-141">System.Boolean</span></span>

## <span data-ttu-id="1771a-142">Note</span><span class="sxs-lookup"><span data-stu-id="1771a-142">NOTES</span></span>

## <span data-ttu-id="1771a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1771a-143">RELATED LINKS</span></span>
