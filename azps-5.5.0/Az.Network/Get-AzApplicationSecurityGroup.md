---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193911"
---
# <span data-ttu-id="dd4a3-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd4a3-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="dd4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4a3-103">Ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-103">Gets an application security group.</span></span>

## <span data-ttu-id="dd4a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd4a3-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd4a3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="dd4a3-106">Il **cmdlet Get-AzApplicationSecurityGroup** ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="dd4a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="dd4a3-108">Esempio 1: Recuperare tutti i gruppi di sicurezza delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="dd4a3-109">Il comando precedente restituisce tutti i gruppi di sicurezza delle applicazioni nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="dd4a3-110">Esempio 2: Recuperare i gruppi di sicurezza delle applicazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="dd4a3-111">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione che appartengono al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="dd4a3-112">Esempio 3: Recuperare uno specifico gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="dd4a3-113">Il comando precedente restituisce il gruppo di sicurezza dell'applicazione MyApplicationSecurityGroup sotto il gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="dd4a3-114">Esempio 4: Recuperare i gruppi di sicurezza delle applicazioni con i filtri.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="dd4a3-115">Il comando precedente restituisce tutti i gruppi di sicurezza delle applicazioni che iniziano con "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="dd4a3-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="dd4a3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd4a3-116">PARAMETERS</span></span>

### <span data-ttu-id="dd4a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4a3-117">-DefaultProfile</span></span>
<span data-ttu-id="dd4a3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd4a3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dd4a3-119">-Name</span></span>
<span data-ttu-id="dd4a3-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-120">The resource name.</span></span>

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

### <span data-ttu-id="dd4a3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4a3-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd4a3-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-122">The resource group name.</span></span>

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

### <span data-ttu-id="dd4a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4a3-123">CommonParameters</span></span>
<span data-ttu-id="dd4a3-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4a3-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd4a3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4a3-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd4a3-126">INPUTS</span></span>

### <span data-ttu-id="dd4a3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dd4a3-127">System.String</span></span>

## <span data-ttu-id="dd4a3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd4a3-128">OUTPUTS</span></span>

### <span data-ttu-id="dd4a3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd4a3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="dd4a3-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd4a3-130">NOTES</span></span>

## <span data-ttu-id="dd4a3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd4a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd4a3-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd4a3-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="dd4a3-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dd4a3-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="dd4a3-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd4a3-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="dd4a3-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd4a3-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
