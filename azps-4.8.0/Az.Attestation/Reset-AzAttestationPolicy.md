---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188601"
---
# <span data-ttu-id="c2e80-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e80-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="c2e80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2e80-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e80-103">Reimposta i criteri di un tenant in Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="c2e80-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="c2e80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2e80-104">SYNTAX</span></span>

### <span data-ttu-id="c2e80-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e80-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2e80-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2e80-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e80-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2e80-107">DESCRIPTION</span></span>
<span data-ttu-id="c2e80-108">Il cmdlet Reset-AzAttestationPolicy Reimposta i criteri di attestazione definiti dall'utente da un tenant in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="c2e80-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="c2e80-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2e80-109">EXAMPLES</span></span>

### <span data-ttu-id="c2e80-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2e80-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="c2e80-111">Reimpostare i criteri per l'impostazione predefinita per il provider di attestazione *pshtest* per il tipo Tee *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="c2e80-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="c2e80-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c2e80-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="c2e80-113">Se il provider di attestazione *pshtest* è configurato per l'uso del modello di attendibilità isolato, reimpostare il criterio per l'impostazione predefinita per il tipo di tee *SgxEnclave* includendo un criterio firmato.</span><span class="sxs-lookup"><span data-stu-id="c2e80-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="c2e80-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2e80-114">PARAMETERS</span></span>

### <span data-ttu-id="c2e80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e80-115">-DefaultProfile</span></span>
<span data-ttu-id="c2e80-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e80-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e80-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2e80-117">-Name</span></span>
<span data-ttu-id="c2e80-118">Specifica un nome del tenant.</span><span class="sxs-lookup"><span data-stu-id="c2e80-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="c2e80-119">Questo cmdlet Reimposta i criteri di attestazione per il tenant specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c2e80-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e80-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2e80-120">-PassThru</span></span>
<span data-ttu-id="c2e80-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c2e80-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c2e80-122">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="c2e80-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c2e80-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="c2e80-123">-Policy</span></span>
<span data-ttu-id="c2e80-124">Specifica il token Web JSON che descrive il documento di criteri da reimpostare.</span><span class="sxs-lookup"><span data-stu-id="c2e80-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e80-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e80-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2e80-126">Specifica il nome del gruppo di risorse di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="c2e80-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e80-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2e80-127">-ResourceId</span></span>
<span data-ttu-id="c2e80-128">Specifica il ResourceID di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="c2e80-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e80-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="c2e80-129">-Tee</span></span>
<span data-ttu-id="c2e80-130">Specifica un tipo di ambiente di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="c2e80-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="c2e80-131">Supportiamo quattro tipi di ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="c2e80-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e80-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2e80-132">-Confirm</span></span>
<span data-ttu-id="c2e80-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e80-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e80-134">-WhatIf</span></span>
<span data-ttu-id="c2e80-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2e80-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e80-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2e80-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e80-137">CommonParameters</span></span>
<span data-ttu-id="c2e80-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e80-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2e80-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e80-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2e80-140">INPUTS</span></span>

### <span data-ttu-id="c2e80-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c2e80-141">System.String</span></span>

## <span data-ttu-id="c2e80-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2e80-142">OUTPUTS</span></span>

### <span data-ttu-id="c2e80-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2e80-143">System.Boolean</span></span>

## <span data-ttu-id="c2e80-144">Note</span><span class="sxs-lookup"><span data-stu-id="c2e80-144">NOTES</span></span>

## <span data-ttu-id="c2e80-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2e80-145">RELATED LINKS</span></span>