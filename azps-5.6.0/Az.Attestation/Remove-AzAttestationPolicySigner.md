---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: e0b86a1cd7c3e1355cfc760fecc257b3cde87561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966813"
---
# <span data-ttu-id="6c082-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="6c082-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="6c082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c082-102">SYNOPSIS</span></span>
<span data-ttu-id="6c082-103">Rimuove un firmatario di criteri attendibili per un tenant in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="6c082-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="6c082-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c082-104">SYNTAX</span></span>

### <span data-ttu-id="6c082-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c082-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c082-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c082-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c082-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c082-107">DESCRIPTION</span></span>
<span data-ttu-id="6c082-108">Il cmdlet Remove-AzAttestationPolicySigner rimuove un firmatario di criteri attendibili per un tenant in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="6c082-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="6c082-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c082-109">EXAMPLES</span></span>

### <span data-ttu-id="6c082-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c082-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="6c082-111">Rimuovere un firmatario attendibile per il provider di attestazione *denominato pshtest.*</span><span class="sxs-lookup"><span data-stu-id="6c082-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="6c082-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c082-112">PARAMETERS</span></span>

### <span data-ttu-id="6c082-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c082-113">-DefaultProfile</span></span>
<span data-ttu-id="6c082-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c082-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c082-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6c082-115">-Name</span></span>
<span data-ttu-id="6c082-116">Specifica il nome di un provider di attestazioni.</span><span class="sxs-lookup"><span data-stu-id="6c082-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="6c082-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c082-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c082-118">Specifica il nome del gruppo di risorse di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="6c082-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="6c082-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c082-119">-ResourceId</span></span>
<span data-ttu-id="6c082-120">Specifica l'ID Risorsa di un provider di attestazioni.</span><span class="sxs-lookup"><span data-stu-id="6c082-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="6c082-121">-Firmatario</span><span class="sxs-lookup"><span data-stu-id="6c082-121">-Signer</span></span>
<span data-ttu-id="6c082-122">Specifica il token Web JSON RFC7519 contenente un'attestazione denominata "maa-policyCertificate" il cui valore è una chiave Web JSON RFC7517 che contiene una chiave di firma attendibile da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6c082-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="6c082-123">Il valore RFC7519 JWT deve essere firmato con una delle chiavi di firma attendibili esistenti.</span><span class="sxs-lookup"><span data-stu-id="6c082-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="6c082-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c082-124">-Confirm</span></span>
<span data-ttu-id="6c082-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c082-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c082-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c082-126">-WhatIf</span></span>
<span data-ttu-id="6c082-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c082-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c082-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c082-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c082-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c082-129">CommonParameters</span></span>
<span data-ttu-id="6c082-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c082-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c082-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c082-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c082-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c082-132">INPUTS</span></span>

### <span data-ttu-id="6c082-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6c082-133">System.String</span></span>

## <span data-ttu-id="6c082-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c082-134">OUTPUTS</span></span>

### <span data-ttu-id="6c082-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="6c082-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="6c082-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c082-136">NOTES</span></span>

## <span data-ttu-id="6c082-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c082-137">RELATED LINKS</span></span>
