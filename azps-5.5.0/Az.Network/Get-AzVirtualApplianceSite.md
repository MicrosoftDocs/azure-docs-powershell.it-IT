---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193726"
---
# <span data-ttu-id="48185-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="48185-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="48185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48185-102">SYNOPSIS</span></span>
<span data-ttu-id="48185-103">Ottenere o elencare i siti connessi alle risorse di Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="48185-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="48185-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48185-104">SYNTAX</span></span>

### <span data-ttu-id="48185-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48185-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48185-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48185-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48185-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48185-107">DESCRIPTION</span></span>
<span data-ttu-id="48185-108">LGet-AzVirtualApplianceSite ottiene o elenca i siti connessi a una o più risorse di Appliance virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="48185-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="48185-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48185-109">EXAMPLES</span></span>

### <span data-ttu-id="48185-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48185-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="48185-111">Ottenere una risorsa del sito Appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="48185-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="48185-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="48185-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="48185-113">Elencare le risorse del sito Appliance virtuale in un'appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="48185-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="48185-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48185-114">PARAMETERS</span></span>

### <span data-ttu-id="48185-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48185-115">-DefaultProfile</span></span>
<span data-ttu-id="48185-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48185-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48185-117">-Name</span><span class="sxs-lookup"><span data-stu-id="48185-117">-Name</span></span>
<span data-ttu-id="48185-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="48185-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48185-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="48185-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="48185-120">Appliance virtuale di rete a cui è collegato il sito.</span><span class="sxs-lookup"><span data-stu-id="48185-120">The Network Virtual Appliance that the site is attached.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48185-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48185-121">-ResourceGroupName</span></span>
<span data-ttu-id="48185-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48185-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48185-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48185-123">-ResourceId</span></span>
<span data-ttu-id="48185-124">ID della risorsa del sito dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="48185-124">The resource Id of the Virtual Appliance Site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48185-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48185-125">CommonParameters</span></span>
<span data-ttu-id="48185-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48185-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48185-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48185-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48185-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="48185-128">INPUTS</span></span>

### <span data-ttu-id="48185-129">System.String</span><span class="sxs-lookup"><span data-stu-id="48185-129">System.String</span></span>

## <span data-ttu-id="48185-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48185-130">OUTPUTS</span></span>

### <span data-ttu-id="48185-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="48185-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="48185-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="48185-132">NOTES</span></span>

## <span data-ttu-id="48185-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48185-133">RELATED LINKS</span></span>
