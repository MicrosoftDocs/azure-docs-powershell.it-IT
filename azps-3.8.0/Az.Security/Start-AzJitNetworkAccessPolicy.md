---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e8ad97b08b85dd79f1fef4457a2825eb9ad32a16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021719"
---
# <span data-ttu-id="6fda2-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6fda2-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="6fda2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fda2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fda2-103">Richiama una richiesta di accesso temporaneo alla rete.</span><span class="sxs-lookup"><span data-stu-id="6fda2-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="6fda2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fda2-104">SYNTAX</span></span>

### <span data-ttu-id="6fda2-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6fda2-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fda2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fda2-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fda2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6fda2-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fda2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fda2-108">DESCRIPTION</span></span>
<span data-ttu-id="6fda2-109">Richiama una richiesta di accesso temporaneo alla rete.</span><span class="sxs-lookup"><span data-stu-id="6fda2-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="6fda2-110">La richiesta viene convalidata rispetto ai criteri di accesso alla rete JIT configurati e, se consentito, apre una connessione di rete in base alla richiesta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6fda2-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="6fda2-111">La richiesta verrà registrata nel criterio per la revisione successiva e verrà terminata quando verrà superata la durata specificata.</span><span class="sxs-lookup"><span data-stu-id="6fda2-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="6fda2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fda2-112">EXAMPLES</span></span>

### <span data-ttu-id="6fda2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fda2-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="6fda2-114">Apre una connessione di rete in base ai dati della richiesta di connessione specificati.</span><span class="sxs-lookup"><span data-stu-id="6fda2-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="6fda2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fda2-115">PARAMETERS</span></span>

### <span data-ttu-id="6fda2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fda2-116">-DefaultProfile</span></span>
<span data-ttu-id="6fda2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fda2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fda2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fda2-118">-InputObject</span></span>
<span data-ttu-id="6fda2-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="6fda2-119">Input Object.</span></span>

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

### <span data-ttu-id="6fda2-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6fda2-120">-Location</span></span>
<span data-ttu-id="6fda2-121">Posizione.</span><span class="sxs-lookup"><span data-stu-id="6fda2-121">Location.</span></span>

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

### <span data-ttu-id="6fda2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fda2-122">-Name</span></span>
<span data-ttu-id="6fda2-123">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="6fda2-123">Resource name.</span></span>

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

### <span data-ttu-id="6fda2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fda2-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fda2-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6fda2-125">Resource group name.</span></span>

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

### <span data-ttu-id="6fda2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fda2-126">-ResourceId</span></span>
<span data-ttu-id="6fda2-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6fda2-127">Resource ID.</span></span>

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

### <span data-ttu-id="6fda2-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6fda2-128">-VirtualMachine</span></span>
<span data-ttu-id="6fda2-129">Provisioning automatico.</span><span class="sxs-lookup"><span data-stu-id="6fda2-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="6fda2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6fda2-130">-Confirm</span></span>
<span data-ttu-id="6fda2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fda2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fda2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fda2-132">-WhatIf</span></span>
<span data-ttu-id="6fda2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fda2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fda2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fda2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fda2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fda2-135">CommonParameters</span></span>
<span data-ttu-id="6fda2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fda2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fda2-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fda2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fda2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fda2-138">INPUTS</span></span>

### <span data-ttu-id="6fda2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6fda2-139">System.String</span></span>

### <span data-ttu-id="6fda2-140">Microsoft. Azure. Commands. Security. Cmdlets. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="6fda2-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="6fda2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fda2-141">OUTPUTS</span></span>

### <span data-ttu-id="6fda2-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6fda2-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="6fda2-143">Note</span><span class="sxs-lookup"><span data-stu-id="6fda2-143">NOTES</span></span>

## <span data-ttu-id="6fda2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fda2-144">RELATED LINKS</span></span>
