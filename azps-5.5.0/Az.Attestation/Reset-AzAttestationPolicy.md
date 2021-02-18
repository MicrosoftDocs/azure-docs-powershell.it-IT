---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201238"
---
# <span data-ttu-id="51a1c-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="51a1c-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="51a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="51a1c-103">Reimposta il criterio da un tenant in Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="51a1c-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="51a1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51a1c-104">SYNTAX</span></span>

### <span data-ttu-id="51a1c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51a1c-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51a1c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51a1c-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51a1c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="51a1c-108">Il Reset-AzAttestationPolicy cmdlet reimposta i criteri di attestazione definiti dall'utente da un tenant in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="51a1c-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="51a1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51a1c-109">EXAMPLES</span></span>

### <span data-ttu-id="51a1c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51a1c-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="51a1c-111">Reimpostare il criterio predefinito per il *test pshtest* del provider di attestazione per il tipo di tee *SgxEnclave.*</span><span class="sxs-lookup"><span data-stu-id="51a1c-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="51a1c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="51a1c-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="51a1c-113">Se il *test Pshtest* del provider di attestazione è configurato per l'uso del modello di attendibilità isolata, reimpostare il criterio sul valore predefinito per il tipo di tee *SgxEnclave* includendo un criterio firmato.</span><span class="sxs-lookup"><span data-stu-id="51a1c-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="51a1c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51a1c-114">PARAMETERS</span></span>

### <span data-ttu-id="51a1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a1c-115">-DefaultProfile</span></span>
<span data-ttu-id="51a1c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51a1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51a1c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="51a1c-117">-Name</span></span>
<span data-ttu-id="51a1c-118">Specifica un nome del tenant.</span><span class="sxs-lookup"><span data-stu-id="51a1c-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="51a1c-119">Questo cmdlet reimposta i criteri di attestazione per il tenant specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a1c-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a1c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51a1c-120">-PassThru</span></span>
<span data-ttu-id="51a1c-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="51a1c-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="51a1c-122">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="51a1c-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="51a1c-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="51a1c-123">-Policy</span></span>
<span data-ttu-id="51a1c-124">Specifica il token Web JSON che descrive il documento dei criteri da reimpostare.</span><span class="sxs-lookup"><span data-stu-id="51a1c-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="51a1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="51a1c-126">Specifica il nome del gruppo di risorse di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="51a1c-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="51a1c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51a1c-127">-ResourceId</span></span>
<span data-ttu-id="51a1c-128">Specifica l'ID Risorsa di un provider di attestazioni.</span><span class="sxs-lookup"><span data-stu-id="51a1c-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="51a1c-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="51a1c-129">-Tee</span></span>
<span data-ttu-id="51a1c-130">Specifica un tipo di ambiente di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="51a1c-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="51a1c-131">Sono supportati quattro tipi di ambiente: SgxEnclave, OpenEnclave, CyRes Sistema e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="51a1c-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="51a1c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51a1c-132">-Confirm</span></span>
<span data-ttu-id="51a1c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a1c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a1c-134">-WhatIf</span></span>
<span data-ttu-id="51a1c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51a1c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51a1c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51a1c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51a1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a1c-137">CommonParameters</span></span>
<span data-ttu-id="51a1c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a1c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51a1c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a1c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="51a1c-140">INPUTS</span></span>

### <span data-ttu-id="51a1c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="51a1c-141">System.String</span></span>

## <span data-ttu-id="51a1c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51a1c-142">OUTPUTS</span></span>

### <span data-ttu-id="51a1c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51a1c-143">System.Boolean</span></span>

## <span data-ttu-id="51a1c-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="51a1c-144">NOTES</span></span>

## <span data-ttu-id="51a1c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51a1c-145">RELATED LINKS</span></span>
