---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 2919c007852961386fb1ab444e43d855ced2a8d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964238"
---
# <span data-ttu-id="56184-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="56184-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="56184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56184-102">SYNOPSIS</span></span>
<span data-ttu-id="56184-103">Ottiene l'elenco di tutte le VpnServerConfigurations associate a questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="56184-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="56184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56184-104">SYNTAX</span></span>

### <span data-ttu-id="56184-105">ByVirtualWanName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56184-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56184-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="56184-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56184-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="56184-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56184-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56184-108">DESCRIPTION</span></span>
<span data-ttu-id="56184-109">Il cmdlet **Get-AzVirtualWanVpnServerConfiguration** restituisce l'elenco di tutte le VpnServerConfigurations associate a questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="56184-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="56184-110">ad esempio tutte le VpnServerConfigurations collegate a qualsiasi P2SVpnGateways in VirutalHubs di questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="56184-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="56184-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56184-111">EXAMPLES</span></span>

### <span data-ttu-id="56184-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56184-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="56184-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56184-113">PARAMETERS</span></span>

### <span data-ttu-id="56184-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56184-114">-DefaultProfile</span></span>
<span data-ttu-id="56184-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56184-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56184-116">-Name</span><span class="sxs-lookup"><span data-stu-id="56184-116">-Name</span></span>
<span data-ttu-id="56184-117">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="56184-117">The resource name.</span></span>

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

### <span data-ttu-id="56184-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56184-118">-ResourceGroupName</span></span>
<span data-ttu-id="56184-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56184-119">The resource group name.</span></span>

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

### <span data-ttu-id="56184-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56184-120">-ResourceId</span></span>
<span data-ttu-id="56184-121">ID della risorsa Azure per la wan virtuale.</span><span class="sxs-lookup"><span data-stu-id="56184-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="56184-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="56184-122">-VirtualWanObject</span></span>
<span data-ttu-id="56184-123">L'oggetto Wan virtuale.</span><span class="sxs-lookup"><span data-stu-id="56184-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="56184-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56184-124">CommonParameters</span></span>
<span data-ttu-id="56184-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56184-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56184-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56184-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56184-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="56184-127">INPUTS</span></span>

### <span data-ttu-id="56184-128">System.String</span><span class="sxs-lookup"><span data-stu-id="56184-128">System.String</span></span>
<span data-ttu-id="56184-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="56184-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="56184-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56184-130">OUTPUTS</span></span>

### <span data-ttu-id="56184-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="56184-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="56184-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="56184-132">NOTES</span></span>

## <span data-ttu-id="56184-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56184-133">RELATED LINKS</span></span>
