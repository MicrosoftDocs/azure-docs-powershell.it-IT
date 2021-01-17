---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488983"
---
# <span data-ttu-id="f6c63-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f6c63-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="f6c63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6c63-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c63-103">Ottiene le informazioni dettagliate del punto corrente alle connessioni del sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f6c63-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="f6c63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6c63-104">SYNTAX</span></span>

### <span data-ttu-id="f6c63-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6c63-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6c63-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f6c63-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6c63-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f6c63-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c63-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6c63-108">DESCRIPTION</span></span>
<span data-ttu-id="f6c63-109">Il cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** consente di ottenere informazioni dettagliate sulle connessioni del punto corrente a quelle del sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f6c63-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="f6c63-110">Il cliente deve passare l'URL SAS in cui è possibile inserire queste informazioni dettagliate sull'integrità.</span><span class="sxs-lookup"><span data-stu-id="f6c63-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="f6c63-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6c63-111">EXAMPLES</span></span>

### <span data-ttu-id="f6c63-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6c63-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="f6c63-113">Il cmdlet **Get-AzP2sVpnGatewayDetailedConnectionHealth** consente di ottenere informazioni dettagliate sulle connessioni del punto corrente a quelle del sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f6c63-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="f6c63-114">Il cliente può scaricare i dettagli sull'integrità da download di URL SAS passati.</span><span class="sxs-lookup"><span data-stu-id="f6c63-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="f6c63-115">In questo modo verranno visualizzate le informazioni di ogni collegamento al sito con nomi utente, byte in, byte fuori, indirizzo IP allocato e così via.</span><span class="sxs-lookup"><span data-stu-id="f6c63-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="f6c63-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6c63-116">PARAMETERS</span></span>

### <span data-ttu-id="f6c63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c63-117">-DefaultProfile</span></span>
<span data-ttu-id="f6c63-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6c63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6c63-119">-InputObject</span></span>
<span data-ttu-id="f6c63-120">L'oggetto gateway VPN di P2S da modificare</span><span class="sxs-lookup"><span data-stu-id="f6c63-120">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="f6c63-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6c63-121">-Name</span></span>
<span data-ttu-id="f6c63-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f6c63-122">The resource name.</span></span>

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

### <span data-ttu-id="f6c63-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="f6c63-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="f6c63-124">URL di OutputBlob SAS a cui verrà scritta l'integrità della connessione VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="f6c63-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

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

### <span data-ttu-id="f6c63-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6c63-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6c63-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6c63-126">The resource group name.</span></span>

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

### <span data-ttu-id="f6c63-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6c63-127">-ResourceId</span></span>
<span data-ttu-id="f6c63-128">ID risorsa di Azure della P2SVpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="f6c63-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="f6c63-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="f6c63-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="f6c63-130">L'elenco dei nomi utente di P2S VPN da filtrare.</span><span class="sxs-lookup"><span data-stu-id="f6c63-130">The list of P2S vpn user names to filter.</span></span>

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

### <span data-ttu-id="f6c63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c63-131">CommonParameters</span></span>
<span data-ttu-id="f6c63-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c63-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c63-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c63-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6c63-134">INPUTS</span></span>

### <span data-ttu-id="f6c63-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f6c63-135">System.String</span></span>
<span data-ttu-id="f6c63-136">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f6c63-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="f6c63-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6c63-137">OUTPUTS</span></span>

### <span data-ttu-id="f6c63-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f6c63-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="f6c63-139">Note</span><span class="sxs-lookup"><span data-stu-id="f6c63-139">NOTES</span></span>

## <span data-ttu-id="f6c63-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6c63-140">RELATED LINKS</span></span>
