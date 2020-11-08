---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203343"
---
# <span data-ttu-id="b8919-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8919-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="b8919-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8919-102">SYNOPSIS</span></span>
<span data-ttu-id="b8919-103">Ottiene una risorsa CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8919-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="b8919-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8919-104">SYNTAX</span></span>

### <span data-ttu-id="b8919-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b8919-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8919-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8919-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8919-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8919-107">DESCRIPTION</span></span>
<span data-ttu-id="b8919-108">Il cmdlet **Get-AzCustomIpPrefix** ottiene uno o più CustomIpPrefixes in base al set di parametri di input</span><span class="sxs-lookup"><span data-stu-id="b8919-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="b8919-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8919-109">EXAMPLES</span></span>

### <span data-ttu-id="b8919-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b8919-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="b8919-111">Questo comando ottiene una risorsa CustomIpPrefix denominata myCustomIpPrefix nel gruppo di risorse myRg</span><span class="sxs-lookup"><span data-stu-id="b8919-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="b8919-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8919-112">PARAMETERS</span></span>

### <span data-ttu-id="b8919-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8919-113">-DefaultProfile</span></span>
<span data-ttu-id="b8919-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8919-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8919-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8919-115">-Name</span></span>
<span data-ttu-id="b8919-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b8919-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8919-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8919-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8919-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b8919-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8919-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8919-119">-ResourceId</span></span>
<span data-ttu-id="b8919-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b8919-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8919-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8919-121">CommonParameters</span></span>
<span data-ttu-id="b8919-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8919-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8919-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8919-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8919-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8919-124">INPUTS</span></span>

### <span data-ttu-id="b8919-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b8919-125">System.String</span></span>

## <span data-ttu-id="b8919-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8919-126">OUTPUTS</span></span>

### <span data-ttu-id="b8919-127">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8919-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="b8919-128">Note</span><span class="sxs-lookup"><span data-stu-id="b8919-128">NOTES</span></span>

## <span data-ttu-id="b8919-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8919-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8919-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8919-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="b8919-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8919-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="b8919-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b8919-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)