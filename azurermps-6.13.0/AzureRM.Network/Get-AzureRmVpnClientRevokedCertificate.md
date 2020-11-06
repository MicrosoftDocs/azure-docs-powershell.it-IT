---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: bb6a4c13b65697de624e9a9913e2f0f9cc6ea476
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513731"
---
# <span data-ttu-id="4107e-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4107e-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="4107e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4107e-102">SYNOPSIS</span></span>
<span data-ttu-id="4107e-103">Ottiene informazioni sui certificati di revoca del client VPN.</span><span class="sxs-lookup"><span data-stu-id="4107e-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4107e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4107e-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4107e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4107e-105">DESCRIPTION</span></span>
<span data-ttu-id="4107e-106">Il cmdlet **Get-AzureRmVpnClientRevokedCertificate** restituisce informazioni sui certificati di revoca client assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4107e-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="4107e-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="4107e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="4107e-108">**Get-AzureRmVpnClientRevokedCertificate** consente di restituire informazioni su tutti i certificati di revoca del client nel gateway oppure, usando il parametro *VpnClientRevokedCertificateName* , per ottenere informazioni su un singolo certificato.</span><span class="sxs-lookup"><span data-stu-id="4107e-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="4107e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4107e-109">EXAMPLES</span></span>

### <span data-ttu-id="4107e-110">Esempio 1: ottenere informazioni su tutti i certificati di revoca del client</span><span class="sxs-lookup"><span data-stu-id="4107e-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="4107e-111">Questo comando consente di ottenere informazioni su tutti i certificati di revoca client associati al gateway di rete virtuale denominato ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="4107e-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="4107e-112">Esempio 2: ottenere informazioni su specifici certificati di revoca del client</span><span class="sxs-lookup"><span data-stu-id="4107e-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="4107e-113">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="4107e-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="4107e-114">In questo caso, tuttavia, il parametro *VpnClientRevokedCertificateName* viene usato per limitare i dati restituiti a uno specifico certificato revocato dal client: il certificato con il nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="4107e-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="4107e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4107e-115">PARAMETERS</span></span>

### <span data-ttu-id="4107e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4107e-116">-DefaultProfile</span></span>
<span data-ttu-id="4107e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4107e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4107e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4107e-118">-ResourceGroupName</span></span>
<span data-ttu-id="4107e-119">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4107e-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="4107e-120">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4107e-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="4107e-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4107e-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4107e-122">Specifica il nome del gateway di rete virtuale in cui sono assegnate le informazioni del certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="4107e-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="4107e-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="4107e-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="4107e-124">Specifica il nome del certificato del client VPN che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4107e-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4107e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4107e-125">CommonParameters</span></span>
<span data-ttu-id="4107e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4107e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4107e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4107e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4107e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4107e-128">INPUTS</span></span>

### <span data-ttu-id="4107e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4107e-129">System.String</span></span>

## <span data-ttu-id="4107e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4107e-130">OUTPUTS</span></span>

### <span data-ttu-id="4107e-131">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4107e-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="4107e-132">Note</span><span class="sxs-lookup"><span data-stu-id="4107e-132">NOTES</span></span>

## <span data-ttu-id="4107e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4107e-133">RELATED LINKS</span></span>

[<span data-ttu-id="4107e-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4107e-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="4107e-135">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4107e-135">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="4107e-136">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4107e-136">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)

