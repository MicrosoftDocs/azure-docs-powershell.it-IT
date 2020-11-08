---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 35e6496cf8dbbcc9bb183bef2e8c83f7fba4a9b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203162"
---
# <span data-ttu-id="13887-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13887-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="13887-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13887-102">SYNOPSIS</span></span>
<span data-ttu-id="13887-103">Ottiene un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="13887-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="13887-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13887-104">SYNTAX</span></span>

### <span data-ttu-id="13887-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13887-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13887-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13887-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13887-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13887-107">DESCRIPTION</span></span>
<span data-ttu-id="13887-108">Il cmdlet **Get-AzPublicIpPrefix** ottiene uno o più prefissi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13887-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="13887-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13887-109">EXAMPLES</span></span>

### <span data-ttu-id="13887-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13887-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="13887-111">Questo comando ottiene una risorsa prefisso IP pubblico con myPublicIpPrefix1 nel gruppo di risorse myRg</span><span class="sxs-lookup"><span data-stu-id="13887-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="13887-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="13887-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="13887-113">Questo comando consente di ottenere tutte le risorse del prefisso IP pubblico che iniziano con myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="13887-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="13887-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13887-114">PARAMETERS</span></span>

### <span data-ttu-id="13887-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13887-115">-DefaultProfile</span></span>
<span data-ttu-id="13887-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13887-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13887-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="13887-117">-Name</span></span>
<span data-ttu-id="13887-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="13887-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="13887-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13887-119">-ResourceGroupName</span></span>
<span data-ttu-id="13887-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13887-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="13887-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13887-121">-ResourceId</span></span>
<span data-ttu-id="13887-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="13887-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13887-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13887-123">CommonParameters</span></span>
<span data-ttu-id="13887-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13887-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13887-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13887-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13887-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13887-126">INPUTS</span></span>

### <span data-ttu-id="13887-127">System. String</span><span class="sxs-lookup"><span data-stu-id="13887-127">System.String</span></span>

## <span data-ttu-id="13887-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13887-128">OUTPUTS</span></span>

### <span data-ttu-id="13887-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13887-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="13887-130">Note</span><span class="sxs-lookup"><span data-stu-id="13887-130">NOTES</span></span>

## <span data-ttu-id="13887-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13887-131">RELATED LINKS</span></span>

[<span data-ttu-id="13887-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13887-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="13887-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13887-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="13887-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="13887-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
