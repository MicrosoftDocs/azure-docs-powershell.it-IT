---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c385ca902764d6bf9afa3808d718c2ceb5d1357c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191942"
---
# <span data-ttu-id="7c320-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c320-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="7c320-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c320-102">SYNOPSIS</span></span>
<span data-ttu-id="7c320-103">Ottiene i criteri di accesso alla rete JIT</span><span class="sxs-lookup"><span data-stu-id="7c320-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="7c320-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c320-104">SYNTAX</span></span>

### <span data-ttu-id="7c320-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c320-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c320-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="7c320-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c320-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="7c320-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c320-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c320-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c320-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c320-109">DESCRIPTION</span></span>
<span data-ttu-id="7c320-110">I criteri di accesso alla rete just in time (JIT) consentono di definire un criterio l'opzione consente agli utenti semplici di creare una connessione di rete temporanea a una VM.</span><span class="sxs-lookup"><span data-stu-id="7c320-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="7c320-111">Il criterio definisce quali porte, protocolli e indirizzi IP di origine possono richiedere una connessione a una VM e la durata massima prima che la connessione venga chiusa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7c320-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="7c320-112">Nel criterio è anche possibile visualizzare la richiesta di connessione eseguita con questo criterio.</span><span class="sxs-lookup"><span data-stu-id="7c320-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="7c320-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c320-113">EXAMPLES</span></span>

### <span data-ttu-id="7c320-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c320-114">Example 1</span></span>
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

<span data-ttu-id="7c320-115">Ottenere tutte le polizie di accesso alla rete JIT in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="7c320-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="7c320-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c320-116">Example 2</span></span>
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

<span data-ttu-id="7c320-117">Ottenere tutte le polizie di accesso alla rete JIT nel gruppo di risorse "myService1"</span><span class="sxs-lookup"><span data-stu-id="7c320-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="7c320-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7c320-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="7c320-119">Ottiene un criterio di accesso alla rete JIT specifico</span><span class="sxs-lookup"><span data-stu-id="7c320-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="7c320-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c320-120">PARAMETERS</span></span>

### <span data-ttu-id="7c320-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c320-121">-DefaultProfile</span></span>
<span data-ttu-id="7c320-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c320-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c320-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7c320-123">-Location</span></span>
<span data-ttu-id="7c320-124">Posizione.</span><span class="sxs-lookup"><span data-stu-id="7c320-124">Location.</span></span>

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

### <span data-ttu-id="7c320-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c320-125">-Name</span></span>
<span data-ttu-id="7c320-126">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c320-126">Resource name.</span></span>

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

### <span data-ttu-id="7c320-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c320-127">-ResourceGroupName</span></span>
<span data-ttu-id="7c320-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c320-128">Resource group name.</span></span>

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

### <span data-ttu-id="7c320-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c320-129">-ResourceId</span></span>
<span data-ttu-id="7c320-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c320-130">Resource ID.</span></span>

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

### <span data-ttu-id="7c320-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c320-131">CommonParameters</span></span>
<span data-ttu-id="7c320-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c320-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c320-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c320-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c320-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c320-134">INPUTS</span></span>

### <span data-ttu-id="7c320-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7c320-135">System.String</span></span>

## <span data-ttu-id="7c320-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c320-136">OUTPUTS</span></span>

### <span data-ttu-id="7c320-137">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c320-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="7c320-138">Note</span><span class="sxs-lookup"><span data-stu-id="7c320-138">NOTES</span></span>

## <span data-ttu-id="7c320-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c320-139">RELATED LINKS</span></span>
