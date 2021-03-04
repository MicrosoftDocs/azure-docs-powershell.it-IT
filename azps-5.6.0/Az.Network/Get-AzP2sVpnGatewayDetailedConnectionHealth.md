---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 17092ab89ded950678e60b079cd30558f7ce2aac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954253"
---
# <span data-ttu-id="11f5a-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="11f5a-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="11f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="11f5a-103">Recupera le informazioni dettagliate sulle connessioni del punto corrente al sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="11f5a-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="11f5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11f5a-104">SYNTAX</span></span>

### <span data-ttu-id="11f5a-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11f5a-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11f5a-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="11f5a-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f5a-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="11f5a-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11f5a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="11f5a-108">DESCRIPTION</span></span>
<span data-ttu-id="11f5a-109">Il cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** consente di ottenere le informazioni dettagliate sulle connessioni punto a sito correnti da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="11f5a-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="11f5a-110">Il cliente deve superare l'URL della firma di accesso condiviso dove possiamo inserire queste informazioni dettagliate sull'integrità.</span><span class="sxs-lookup"><span data-stu-id="11f5a-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="11f5a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="11f5a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11f5a-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="11f5a-113">Il cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** consente di ottenere le informazioni dettagliate sulle connessioni punto a sito correnti da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="11f5a-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="11f5a-114">Il cliente può scaricare i dettagli sull'integrità dal download dell'URL della firma di accesso condiviso superato.</span><span class="sxs-lookup"><span data-stu-id="11f5a-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="11f5a-115">Verranno visualizzate informazioni su ogni connessione punto a sito con nome utente, byte in, byte in uscita, indirizzo IP allocato e così via.</span><span class="sxs-lookup"><span data-stu-id="11f5a-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="11f5a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11f5a-116">PARAMETERS</span></span>

### <span data-ttu-id="11f5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f5a-117">-DefaultProfile</span></span>
<span data-ttu-id="11f5a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11f5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11f5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11f5a-119">-InputObject</span></span>
<span data-ttu-id="11f5a-120">Oggetto gateway VPN p2s da modificare</span><span class="sxs-lookup"><span data-stu-id="11f5a-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="11f5a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="11f5a-121">-Name</span></span>
<span data-ttu-id="11f5a-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="11f5a-122">The resource name.</span></span>

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

### <span data-ttu-id="11f5a-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="11f5a-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="11f5a-124">URL Sas OutputBlob in cui verrà scritta l'integrità della connessione VPN p2s.</span><span class="sxs-lookup"><span data-stu-id="11f5a-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="11f5a-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11f5a-126">The resource group name.</span></span>

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

### <span data-ttu-id="11f5a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11f5a-127">-ResourceId</span></span>
<span data-ttu-id="11f5a-128">ID della risorsa Azure di P2SVpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="11f5a-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="11f5a-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="11f5a-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="11f5a-130">Elenco dei nomi utente vpn P2S da filtrare.</span><span class="sxs-lookup"><span data-stu-id="11f5a-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f5a-131">CommonParameters</span></span>
<span data-ttu-id="11f5a-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f5a-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f5a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f5a-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="11f5a-134">INPUTS</span></span>

### <span data-ttu-id="11f5a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="11f5a-135">System.String</span></span>
<span data-ttu-id="11f5a-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="11f5a-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="11f5a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11f5a-137">OUTPUTS</span></span>

### <span data-ttu-id="11f5a-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="11f5a-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="11f5a-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="11f5a-139">NOTES</span></span>

## <span data-ttu-id="11f5a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11f5a-140">RELATED LINKS</span></span>
