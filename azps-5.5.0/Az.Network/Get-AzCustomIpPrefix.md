---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203098"
---
# <span data-ttu-id="61d34-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d34-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="61d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d34-102">SYNOPSIS</span></span>
<span data-ttu-id="61d34-103">Ottiene una risorsa CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d34-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="61d34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61d34-104">SYNTAX</span></span>

### <span data-ttu-id="61d34-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61d34-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61d34-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d34-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61d34-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61d34-107">DESCRIPTION</span></span>
<span data-ttu-id="61d34-108">Il cmdlet **Get-AzCustomIpPrefix** ottiene uno o più provider CustomIpPrefixes in base al set di parametri di input</span><span class="sxs-lookup"><span data-stu-id="61d34-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="61d34-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61d34-109">EXAMPLES</span></span>

### <span data-ttu-id="61d34-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61d34-110">Example 1</span></span>
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

<span data-ttu-id="61d34-111">Questo comando ottiene una risorsa CustomIpPrefix denominata myCustomIpPrefix nel gruppo di risorse myRg</span><span class="sxs-lookup"><span data-stu-id="61d34-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="61d34-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61d34-112">PARAMETERS</span></span>

### <span data-ttu-id="61d34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d34-113">-DefaultProfile</span></span>
<span data-ttu-id="61d34-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61d34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61d34-115">-Name</span><span class="sxs-lookup"><span data-stu-id="61d34-115">-Name</span></span>
<span data-ttu-id="61d34-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="61d34-116">The resource name.</span></span>

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

### <span data-ttu-id="61d34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d34-117">-ResourceGroupName</span></span>
<span data-ttu-id="61d34-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61d34-118">The resource group name.</span></span>

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

### <span data-ttu-id="61d34-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61d34-119">-ResourceId</span></span>
<span data-ttu-id="61d34-120">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="61d34-120">The resource id.</span></span>

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

### <span data-ttu-id="61d34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d34-121">CommonParameters</span></span>
<span data-ttu-id="61d34-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d34-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61d34-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d34-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="61d34-124">INPUTS</span></span>

### <span data-ttu-id="61d34-125">System.String</span><span class="sxs-lookup"><span data-stu-id="61d34-125">System.String</span></span>

## <span data-ttu-id="61d34-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61d34-126">OUTPUTS</span></span>

### <span data-ttu-id="61d34-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d34-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="61d34-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="61d34-128">NOTES</span></span>

## <span data-ttu-id="61d34-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61d34-129">RELATED LINKS</span></span>

[<span data-ttu-id="61d34-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d34-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="61d34-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d34-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="61d34-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="61d34-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)