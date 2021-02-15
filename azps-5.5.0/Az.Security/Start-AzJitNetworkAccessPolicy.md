---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208203"
---
# <span data-ttu-id="fc90b-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fc90b-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="fc90b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc90b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc90b-103">Richiama una richiesta di accesso temporaneo alla rete.</span><span class="sxs-lookup"><span data-stu-id="fc90b-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="fc90b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc90b-104">SYNTAX</span></span>

### <span data-ttu-id="fc90b-105">ResourceGroupLevelResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc90b-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc90b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc90b-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc90b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc90b-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc90b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc90b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc90b-109">Richiama una richiesta di accesso temporaneo alla rete.</span><span class="sxs-lookup"><span data-stu-id="fc90b-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="fc90b-110">La richiesta viene convalidata in base al criterio di accesso di rete JIT configurato e, se consentito, apre una connessione di rete in base alla richiesta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fc90b-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="fc90b-111">La richiesta verrà registrata nel criterio per un'analisi successiva e verrà terminata quando verrà superata la durata specificata.</span><span class="sxs-lookup"><span data-stu-id="fc90b-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="fc90b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc90b-112">EXAMPLES</span></span>

### <span data-ttu-id="fc90b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc90b-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="fc90b-114">Apre una connessione di rete per 1 ora sulla porta 22 dall'IP pubblico (non visualizzata).</span><span class="sxs-lookup"><span data-stu-id="fc90b-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="fc90b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc90b-115">PARAMETERS</span></span>

### <span data-ttu-id="fc90b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc90b-116">-DefaultProfile</span></span>
<span data-ttu-id="fc90b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc90b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc90b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc90b-118">-InputObject</span></span>
<span data-ttu-id="fc90b-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="fc90b-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc90b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fc90b-120">-Location</span></span>
<span data-ttu-id="fc90b-121">Posizione.</span><span class="sxs-lookup"><span data-stu-id="fc90b-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc90b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fc90b-122">-Name</span></span>
<span data-ttu-id="fc90b-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc90b-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc90b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc90b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc90b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc90b-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc90b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc90b-126">-ResourceId</span></span>
<span data-ttu-id="fc90b-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc90b-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc90b-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fc90b-128">-VirtualMachine</span></span>
<span data-ttu-id="fc90b-129">Provisioning automatico.</span><span class="sxs-lookup"><span data-stu-id="fc90b-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc90b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc90b-130">-Confirm</span></span>
<span data-ttu-id="fc90b-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc90b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc90b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc90b-132">-WhatIf</span></span>
<span data-ttu-id="fc90b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc90b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc90b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc90b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc90b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc90b-135">CommonParameters</span></span>
<span data-ttu-id="fc90b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc90b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc90b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc90b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc90b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc90b-138">INPUTS</span></span>

### <span data-ttu-id="fc90b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fc90b-139">System.String</span></span>

### <span data-ttu-id="fc90b-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="fc90b-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="fc90b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc90b-141">OUTPUTS</span></span>

### <span data-ttu-id="fc90b-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fc90b-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="fc90b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc90b-143">NOTES</span></span>

## <span data-ttu-id="fc90b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc90b-144">RELATED LINKS</span></span>
