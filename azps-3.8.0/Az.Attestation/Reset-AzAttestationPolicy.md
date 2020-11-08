---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020684"
---
# <span data-ttu-id="28ff3-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="28ff3-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="28ff3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="28ff3-103">Reimposta i criteri di un tenant in Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="28ff3-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="28ff3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28ff3-104">SYNTAX</span></span>

### <span data-ttu-id="28ff3-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28ff3-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28ff3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28ff3-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28ff3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28ff3-107">DESCRIPTION</span></span>
<span data-ttu-id="28ff3-108">Il cmdlet Reset-AzAttestationPolicy Reimposta i criteri di attestazione definiti dall'utente da un tenant in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="28ff3-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="28ff3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28ff3-109">EXAMPLES</span></span>

### <span data-ttu-id="28ff3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28ff3-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="28ff3-111">Reimpostare i criteri per l'impostazione predefinita per il provider di attestazione *pshtest* per il tipo Tee *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="28ff3-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="28ff3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28ff3-112">PARAMETERS</span></span>

### <span data-ttu-id="28ff3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ff3-113">-DefaultProfile</span></span>
<span data-ttu-id="28ff3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28ff3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28ff3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="28ff3-115">-Name</span></span>
<span data-ttu-id="28ff3-116">Specifica un nome del tenant.</span><span class="sxs-lookup"><span data-stu-id="28ff3-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="28ff3-117">Questo cmdlet Reimposta i criteri di attestazione per il tenant specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="28ff3-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="28ff3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28ff3-118">-PassThru</span></span>
<span data-ttu-id="28ff3-119">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="28ff3-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="28ff3-120">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="28ff3-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="28ff3-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="28ff3-121">-Policy</span></span>
<span data-ttu-id="28ff3-122">Specifica il token Web JSON che descrive il documento di criteri da reimpostare.</span><span class="sxs-lookup"><span data-stu-id="28ff3-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="28ff3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ff3-123">-ResourceGroupName</span></span>
<span data-ttu-id="28ff3-124">Specifica il nome del gruppo di risorse di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="28ff3-124">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="28ff3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28ff3-125">-ResourceId</span></span>
<span data-ttu-id="28ff3-126">Specifica il ResourceID di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="28ff3-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="28ff3-127">-Tee</span><span class="sxs-lookup"><span data-stu-id="28ff3-127">-Tee</span></span>
<span data-ttu-id="28ff3-128">Specifica un tipo di ambiente di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="28ff3-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="28ff3-129">Supportiamo quattro tipi di ambiente: SgxEnclave, OpenEnclave, CyResComponent e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="28ff3-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="28ff3-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28ff3-130">-Confirm</span></span>
<span data-ttu-id="28ff3-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28ff3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28ff3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ff3-132">-WhatIf</span></span>
<span data-ttu-id="28ff3-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28ff3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28ff3-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28ff3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28ff3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ff3-135">CommonParameters</span></span>
<span data-ttu-id="28ff3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ff3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ff3-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28ff3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ff3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28ff3-138">INPUTS</span></span>

### <span data-ttu-id="28ff3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="28ff3-139">System.String</span></span>

## <span data-ttu-id="28ff3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28ff3-140">OUTPUTS</span></span>

### <span data-ttu-id="28ff3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28ff3-141">System.Boolean</span></span>

## <span data-ttu-id="28ff3-142">Note</span><span class="sxs-lookup"><span data-stu-id="28ff3-142">NOTES</span></span>

## <span data-ttu-id="28ff3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28ff3-143">RELATED LINKS</span></span>
