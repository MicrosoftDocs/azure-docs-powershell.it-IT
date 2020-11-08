---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189004"
---
# <span data-ttu-id="ef921-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ef921-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="ef921-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef921-102">SYNOPSIS</span></span>
<span data-ttu-id="ef921-103">Ottenere o elencare i siti connessi alle risorse di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="ef921-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="ef921-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef921-104">SYNTAX</span></span>

### <span data-ttu-id="ef921-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef921-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef921-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef921-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef921-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef921-107">DESCRIPTION</span></span>
<span data-ttu-id="ef921-108">La Get-AzVirtualApplianceSite Ottiene o elenca i siti connessi a una o più risorse di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="ef921-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="ef921-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef921-109">EXAMPLES</span></span>

### <span data-ttu-id="ef921-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef921-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="ef921-111">Ottenere una risorsa sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="ef921-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="ef921-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ef921-112">Example 2</span></span>
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

<span data-ttu-id="ef921-113">Elencare le risorse del sito di Virtual Appliance in una appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="ef921-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="ef921-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef921-114">PARAMETERS</span></span>

### <span data-ttu-id="ef921-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef921-115">-DefaultProfile</span></span>
<span data-ttu-id="ef921-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef921-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef921-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef921-117">-Name</span></span>
<span data-ttu-id="ef921-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ef921-118">The resource name.</span></span>

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

### <span data-ttu-id="ef921-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="ef921-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="ef921-120">L'appliance virtuale di rete a cui è associato il sito.</span><span class="sxs-lookup"><span data-stu-id="ef921-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="ef921-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef921-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef921-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ef921-122">The resource group name.</span></span>

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

### <span data-ttu-id="ef921-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef921-123">-ResourceId</span></span>
<span data-ttu-id="ef921-124">ID risorsa del sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="ef921-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="ef921-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef921-125">CommonParameters</span></span>
<span data-ttu-id="ef921-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef921-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef921-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef921-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef921-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef921-128">INPUTS</span></span>

### <span data-ttu-id="ef921-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef921-129">System.String</span></span>

## <span data-ttu-id="ef921-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef921-130">OUTPUTS</span></span>

### <span data-ttu-id="ef921-131">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ef921-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="ef921-132">Note</span><span class="sxs-lookup"><span data-stu-id="ef921-132">NOTES</span></span>

## <span data-ttu-id="ef921-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef921-133">RELATED LINKS</span></span>
