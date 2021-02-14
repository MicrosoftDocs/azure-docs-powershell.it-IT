---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e82c540b946408671c424a1f86d3266a7e6d6906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176335"
---
# <span data-ttu-id="38edd-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38edd-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="38edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38edd-102">SYNOPSIS</span></span>
<span data-ttu-id="38edd-103">Recupera i criteri di accesso di rete JIT</span><span class="sxs-lookup"><span data-stu-id="38edd-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="38edd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38edd-104">SYNTAX</span></span>

### <span data-ttu-id="38edd-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38edd-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38edd-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="38edd-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38edd-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="38edd-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38edd-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38edd-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38edd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38edd-109">DESCRIPTION</span></span>
<span data-ttu-id="38edd-110">I criteri di accesso di rete Just In Time (JIT) consentono di definire un criterio per consentire agli utenti semplici di creare una connessione di rete temporanea a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="38edd-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="38edd-111">Il criterio definisce quali porte, protocollo e indirizzi IP di origine possono richiedere una connessione a una macchina virtuale e la durata massima prima che la connessione venga chiusa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="38edd-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="38edd-112">Nei criteri è anche possibile visualizzare la richiesta di connessione effettuata con questo criterio.</span><span class="sxs-lookup"><span data-stu-id="38edd-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="38edd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38edd-113">EXAMPLES</span></span>

### <span data-ttu-id="38edd-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38edd-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="38edd-115">Ottenere tutti i criteri di accesso alla rete JIT in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="38edd-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="38edd-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38edd-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="38edd-117">Ottenere tutti i criteri di accesso alla rete JIT nel gruppo di risorse "myService1"</span><span class="sxs-lookup"><span data-stu-id="38edd-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="38edd-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="38edd-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="38edd-119">Ottiene uno specifico criterio di accesso alla rete JIT</span><span class="sxs-lookup"><span data-stu-id="38edd-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="38edd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38edd-120">PARAMETERS</span></span>

### <span data-ttu-id="38edd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38edd-121">-DefaultProfile</span></span>
<span data-ttu-id="38edd-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38edd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38edd-123">-Location</span><span class="sxs-lookup"><span data-stu-id="38edd-123">-Location</span></span>
<span data-ttu-id="38edd-124">Posizione.</span><span class="sxs-lookup"><span data-stu-id="38edd-124">Location.</span></span>

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

### <span data-ttu-id="38edd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="38edd-125">-Name</span></span>
<span data-ttu-id="38edd-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="38edd-126">Resource name.</span></span>

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

### <span data-ttu-id="38edd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38edd-127">-ResourceGroupName</span></span>
<span data-ttu-id="38edd-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38edd-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38edd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38edd-129">-ResourceId</span></span>
<span data-ttu-id="38edd-130">ID risorsa della risorsa Criteri di accesso di rete jit.</span><span class="sxs-lookup"><span data-stu-id="38edd-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="38edd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38edd-131">CommonParameters</span></span>
<span data-ttu-id="38edd-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38edd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38edd-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38edd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38edd-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="38edd-134">INPUTS</span></span>

### <span data-ttu-id="38edd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="38edd-135">System.String</span></span>

## <span data-ttu-id="38edd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38edd-136">OUTPUTS</span></span>

### <span data-ttu-id="38edd-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38edd-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="38edd-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="38edd-138">NOTES</span></span>

## <span data-ttu-id="38edd-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38edd-139">RELATED LINKS</span></span>
