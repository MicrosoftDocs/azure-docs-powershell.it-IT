---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: 62e549ef01f77382226eaf83784add7005516230
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016206"
---
# <span data-ttu-id="e9e07-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e9e07-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="e9e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e07-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e07-103">Ottenere o elencare i siti connessi alle risorse di Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="e9e07-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="e9e07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9e07-104">SYNTAX</span></span>

### <span data-ttu-id="e9e07-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9e07-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9e07-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9e07-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e07-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9e07-107">DESCRIPTION</span></span>
<span data-ttu-id="e9e07-108">LGet-AzVirtualApplianceSite ottiene o elenca i siti connessi a una o più risorse di Appliance virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="e9e07-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="e9e07-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9e07-109">EXAMPLES</span></span>

### <span data-ttu-id="e9e07-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9e07-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="e9e07-111">Ottenere una risorsa del sito Appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9e07-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="e9e07-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e9e07-112">Example 2</span></span>
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

<span data-ttu-id="e9e07-113">Elencare le risorse del sito Appliance virtuale in un'appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="e9e07-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="e9e07-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9e07-114">PARAMETERS</span></span>

### <span data-ttu-id="e9e07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e07-115">-DefaultProfile</span></span>
<span data-ttu-id="e9e07-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e07-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e9e07-117">-Name</span></span>
<span data-ttu-id="e9e07-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e9e07-118">The resource name.</span></span>

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

### <span data-ttu-id="e9e07-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="e9e07-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="e9e07-120">Appliance virtuale di rete a cui è collegato il sito.</span><span class="sxs-lookup"><span data-stu-id="e9e07-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="e9e07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9e07-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9e07-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9e07-122">The resource group name.</span></span>

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

### <span data-ttu-id="e9e07-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e07-123">-ResourceId</span></span>
<span data-ttu-id="e9e07-124">ID della risorsa del sito dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9e07-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="e9e07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e07-125">CommonParameters</span></span>
<span data-ttu-id="e9e07-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e07-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9e07-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e07-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9e07-128">INPUTS</span></span>

### <span data-ttu-id="e9e07-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9e07-129">System.String</span></span>

## <span data-ttu-id="e9e07-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9e07-130">OUTPUTS</span></span>

### <span data-ttu-id="e9e07-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="e9e07-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="e9e07-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9e07-132">NOTES</span></span>

## <span data-ttu-id="e9e07-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9e07-133">RELATED LINKS</span></span>
