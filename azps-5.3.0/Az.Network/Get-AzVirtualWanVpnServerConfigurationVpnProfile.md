---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379732"
---
# <span data-ttu-id="dc37a-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="dc37a-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="dc37a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc37a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc37a-103">Genera e Scarica il profilo VPN a livello di VirtualWan-VpnServerConfiguration per la configurazione di Point to site client.</span><span class="sxs-lookup"><span data-stu-id="dc37a-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="dc37a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc37a-104">SYNTAX</span></span>

### <span data-ttu-id="dc37a-105">ByVirtualWanNameByVpnServerConfigurationObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc37a-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc37a-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="dc37a-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc37a-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dc37a-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc37a-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="dc37a-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc37a-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dc37a-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc37a-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="dc37a-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc37a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc37a-111">DESCRIPTION</span></span>
<span data-ttu-id="dc37a-112">Il cmdlet **Get-AzVirtualWanVpnServerConfigurationVpnProfile** consente di generare e scaricare il profilo VPN a livello di VirtualWan-VpnServerConfiguration per la configurazione di Point to site client.</span><span class="sxs-lookup"><span data-stu-id="dc37a-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="dc37a-113">Questa operazione è necessaria per il punto di connettività del sito da Point a client del sito a Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="dc37a-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="dc37a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc37a-114">EXAMPLES</span></span>

### <span data-ttu-id="dc37a-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc37a-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="dc37a-116">Il comando precedente genererà e restituirà l'URL SAS per il cliente per scaricare il profilo VPN a livello di VirtualWan-VpnServerConfiguration per la configurazione di Point to site client.</span><span class="sxs-lookup"><span data-stu-id="dc37a-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="dc37a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc37a-117">PARAMETERS</span></span>

### <span data-ttu-id="dc37a-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="dc37a-118">-AuthenticationMethod</span></span>
<span data-ttu-id="dc37a-119">Metodo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="dc37a-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc37a-120">-DefaultProfile</span></span>
<span data-ttu-id="dc37a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc37a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc37a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc37a-122">-Name</span></span>
<span data-ttu-id="dc37a-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc37a-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc37a-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc37a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc37a-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc37a-126">-ResourceId</span></span>
<span data-ttu-id="dc37a-127">ID risorsa Azure per la rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc37a-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="dc37a-128">-VirtualWanObject</span></span>
<span data-ttu-id="dc37a-129">Oggetto WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc37a-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc37a-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="dc37a-131">VpnServerConfiguration a cui è associato questo VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="dc37a-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dc37a-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="dc37a-133">ID dell'oggetto configurazione del server VPN a cui verrà associata la WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc37a-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc37a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc37a-134">CommonParameters</span></span>
<span data-ttu-id="dc37a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc37a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc37a-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc37a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc37a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc37a-137">INPUTS</span></span>

### <span data-ttu-id="dc37a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dc37a-138">System.String</span></span>
<span data-ttu-id="dc37a-139">Microsoft. Azure. Commands. Network. Models. PSVirtualWan Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc37a-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="dc37a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc37a-140">OUTPUTS</span></span>

### <span data-ttu-id="dc37a-141">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="dc37a-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="dc37a-142">Note</span><span class="sxs-lookup"><span data-stu-id="dc37a-142">NOTES</span></span>

## <span data-ttu-id="dc37a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc37a-143">RELATED LINKS</span></span>
