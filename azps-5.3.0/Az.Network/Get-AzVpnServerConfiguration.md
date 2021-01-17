---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379634"
---
# <span data-ttu-id="44bc4-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="44bc4-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="44bc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="44bc4-103">Ottiene un VpnServerConfiguration esistente per la connettività point to site.</span><span class="sxs-lookup"><span data-stu-id="44bc4-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="44bc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44bc4-104">SYNTAX</span></span>

### <span data-ttu-id="44bc4-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44bc4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44bc4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44bc4-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44bc4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="44bc4-108">Il cmdlet **Get-AzVpnServerConfiguration** restituisce il VpnServerConfiguration esistente per la connettività point to site.</span><span class="sxs-lookup"><span data-stu-id="44bc4-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="44bc4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="44bc4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44bc4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="44bc4-111">Il comando precedente otterrà il VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="44bc4-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="44bc4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44bc4-112">PARAMETERS</span></span>

### <span data-ttu-id="44bc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bc4-113">-DefaultProfile</span></span>
<span data-ttu-id="44bc4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44bc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44bc4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="44bc4-115">-Name</span></span>
<span data-ttu-id="44bc4-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="44bc4-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44bc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="44bc4-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44bc4-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bc4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bc4-119">CommonParameters</span></span>
<span data-ttu-id="44bc4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44bc4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bc4-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44bc4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bc4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44bc4-122">INPUTS</span></span>

### <span data-ttu-id="44bc4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="44bc4-123">None</span></span>

## <span data-ttu-id="44bc4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44bc4-124">OUTPUTS</span></span>

### <span data-ttu-id="44bc4-125">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="44bc4-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="44bc4-126">Note</span><span class="sxs-lookup"><span data-stu-id="44bc4-126">NOTES</span></span>

## <span data-ttu-id="44bc4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44bc4-127">RELATED LINKS</span></span>
