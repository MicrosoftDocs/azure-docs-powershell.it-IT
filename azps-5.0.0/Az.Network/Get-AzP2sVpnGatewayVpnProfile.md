---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202845"
---
# <span data-ttu-id="35824-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="35824-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="35824-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35824-102">SYNOPSIS</span></span>
<span data-ttu-id="35824-103">Genera e restituisce un URL SAS per il cliente per scaricare il profilo VPN per la configurazione di Point to site client per avere la connettività del sito a P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35824-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="35824-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35824-104">SYNTAX</span></span>

### <span data-ttu-id="35824-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35824-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35824-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="35824-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35824-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="35824-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35824-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35824-108">DESCRIPTION</span></span>
<span data-ttu-id="35824-109">Il cmdlet **Get-AzP2sVpnGatewayVpnProfile** consente di generare e ottenere un URL SAS per il cliente per scaricare il profilo VPN per la configurazione di Point to site client per avere la connettività del sito a P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35824-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="35824-110">Scegliere configurazione client del sito usando questo profilo VPN può connettersi solo a questo specifico P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35824-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="35824-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35824-111">EXAMPLES</span></span>

### <span data-ttu-id="35824-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35824-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="35824-113">Il cmdlet **Get-AzP2sVpnGatewayVpnProfile** consente di generare e ottenere un URL SAS per il cliente per scaricare il profilo VPN per la configurazione di Point to site client per avere la connettività del sito a P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="35824-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="35824-114">ProfileUrl Mostra l'URL SAS da cui il cliente può scaricare il profilo VPN per la configurazione del client Point-to-site.</span><span class="sxs-lookup"><span data-stu-id="35824-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="35824-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35824-115">PARAMETERS</span></span>

### <span data-ttu-id="35824-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="35824-116">-AuthenticationMethod</span></span>
<span data-ttu-id="35824-117">Metodo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="35824-117">Authentication Method</span></span>

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

### <span data-ttu-id="35824-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35824-118">-DefaultProfile</span></span>
<span data-ttu-id="35824-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35824-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35824-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35824-120">-InputObject</span></span>
<span data-ttu-id="35824-121">L'oggetto gateway VPN di P2S da modificare</span><span class="sxs-lookup"><span data-stu-id="35824-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35824-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="35824-122">-Name</span></span>
<span data-ttu-id="35824-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35824-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35824-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35824-124">-ResourceGroupName</span></span>
<span data-ttu-id="35824-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35824-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35824-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35824-126">-ResourceId</span></span>
<span data-ttu-id="35824-127">ID risorsa di Azure della P2SVpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="35824-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35824-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35824-128">CommonParameters</span></span>
<span data-ttu-id="35824-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35824-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35824-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35824-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35824-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35824-131">INPUTS</span></span>

### <span data-ttu-id="35824-132">System. String</span><span class="sxs-lookup"><span data-stu-id="35824-132">System.String</span></span>
<span data-ttu-id="35824-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="35824-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="35824-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35824-134">OUTPUTS</span></span>

### <span data-ttu-id="35824-135">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="35824-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="35824-136">Note</span><span class="sxs-lookup"><span data-stu-id="35824-136">NOTES</span></span>

## <span data-ttu-id="35824-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35824-137">RELATED LINKS</span></span>
