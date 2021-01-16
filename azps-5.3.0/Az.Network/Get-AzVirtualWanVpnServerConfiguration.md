---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379749"
---
# <span data-ttu-id="7daee-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7daee-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="7daee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7daee-102">SYNOPSIS</span></span>
<span data-ttu-id="7daee-103">Ottiene l'elenco di tutti i VpnServerConfigurations associati a questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7daee-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="7daee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7daee-104">SYNTAX</span></span>

### <span data-ttu-id="7daee-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7daee-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7daee-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7daee-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7daee-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="7daee-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7daee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7daee-108">DESCRIPTION</span></span>
<span data-ttu-id="7daee-109">Il cmdlet **Get-AzVirtualWanVpnServerConfiguration** restituirà l'elenco di tutti i VpnServerConfigurations associati a questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7daee-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="7daee-110">vale a dire tutti i VpnServerConfigurations che sono allegati a qualsiasi P2SVpnGateways in VirutalHubs di questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7daee-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="7daee-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7daee-111">EXAMPLES</span></span>

### <span data-ttu-id="7daee-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7daee-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="7daee-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7daee-113">PARAMETERS</span></span>

### <span data-ttu-id="7daee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7daee-114">-DefaultProfile</span></span>
<span data-ttu-id="7daee-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7daee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7daee-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7daee-116">-Name</span></span>
<span data-ttu-id="7daee-117">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7daee-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7daee-118">-ResourceGroupName</span></span>
<span data-ttu-id="7daee-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7daee-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7daee-120">-ResourceId</span></span>
<span data-ttu-id="7daee-121">ID risorsa Azure per la rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="7daee-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7daee-122">-VirtualWanObject</span></span>
<span data-ttu-id="7daee-123">Oggetto WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="7daee-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7daee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7daee-124">CommonParameters</span></span>
<span data-ttu-id="7daee-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7daee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7daee-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7daee-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7daee-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7daee-127">INPUTS</span></span>

### <span data-ttu-id="7daee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7daee-128">System.String</span></span>
<span data-ttu-id="7daee-129">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7daee-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="7daee-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7daee-130">OUTPUTS</span></span>

### <span data-ttu-id="7daee-131">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="7daee-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="7daee-132">Note</span><span class="sxs-lookup"><span data-stu-id="7daee-132">NOTES</span></span>

## <span data-ttu-id="7daee-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7daee-133">RELATED LINKS</span></span>
