---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203432"
---
# <span data-ttu-id="6e798-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e798-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="6e798-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e798-102">SYNOPSIS</span></span>
<span data-ttu-id="6e798-103">Ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e798-103">Gets an application security group.</span></span>

## <span data-ttu-id="6e798-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e798-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e798-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e798-105">DESCRIPTION</span></span>
<span data-ttu-id="6e798-106">Il cmdlet **Get-AzApplicationSecurityGroup** ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e798-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="6e798-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e798-107">EXAMPLES</span></span>

### <span data-ttu-id="6e798-108">Esempio 1: recuperare tutti i gruppi di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e798-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="6e798-109">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6e798-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="6e798-110">Esempio 2: recuperare i gruppi di sicurezza delle applicazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e798-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="6e798-111">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione che appartengono al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6e798-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="6e798-112">Esempio 3: recuperare un gruppo di sicurezza dell'applicazione specifico.</span><span class="sxs-lookup"><span data-stu-id="6e798-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="6e798-113">Il comando precedente restituisce il gruppo di sicurezza dell'applicazione MyApplicationSecurityGroup nel gruppo risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6e798-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="6e798-114">Esempio 4: recuperare i gruppi di sicurezza delle applicazioni tramite filtro.</span><span class="sxs-lookup"><span data-stu-id="6e798-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="6e798-115">Il comando precedente restituisce tutti i gruppi di sicurezza delle applicazioni che iniziano con "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="6e798-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="6e798-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e798-116">PARAMETERS</span></span>

### <span data-ttu-id="6e798-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e798-117">-DefaultProfile</span></span>
<span data-ttu-id="6e798-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e798-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e798-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e798-119">-Name</span></span>
<span data-ttu-id="6e798-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6e798-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6e798-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e798-121">-ResourceGroupName</span></span>
<span data-ttu-id="6e798-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e798-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6e798-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e798-123">CommonParameters</span></span>
<span data-ttu-id="6e798-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e798-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e798-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e798-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e798-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e798-126">INPUTS</span></span>

### <span data-ttu-id="6e798-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6e798-127">System.String</span></span>

## <span data-ttu-id="6e798-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e798-128">OUTPUTS</span></span>

### <span data-ttu-id="6e798-129">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e798-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="6e798-130">Note</span><span class="sxs-lookup"><span data-stu-id="6e798-130">NOTES</span></span>

## <span data-ttu-id="6e798-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e798-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e798-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e798-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="6e798-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e798-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="6e798-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e798-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="6e798-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6e798-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
