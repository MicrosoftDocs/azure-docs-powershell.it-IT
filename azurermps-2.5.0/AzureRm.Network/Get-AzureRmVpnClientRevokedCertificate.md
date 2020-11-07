---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866273"
---
# <span data-ttu-id="1dae0-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1dae0-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1dae0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dae0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dae0-103">Ottiene informazioni sui certificati di revoca del client VPN.</span><span class="sxs-lookup"><span data-stu-id="1dae0-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dae0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dae0-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dae0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dae0-105">DESCRIPTION</span></span>
<span data-ttu-id="1dae0-106">Il cmdlet **Get-AzureRmVpnClientRevokedCertificate** restituisce informazioni sui certificati di revoca client assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1dae0-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="1dae0-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1dae0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="1dae0-108">**Get-AzureRmVpnClientRevokedCertificate** consente di restituire informazioni su tutti i certificati di revoca del client nel gateway oppure, usando il parametro *VpnClientRevokedCertificateName* , per ottenere informazioni su un singolo certificato.</span><span class="sxs-lookup"><span data-stu-id="1dae0-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="1dae0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dae0-109">EXAMPLES</span></span>

### <span data-ttu-id="1dae0-110">Esempio 1: ottenere informazioni su tutti i certificati di revoca del client</span><span class="sxs-lookup"><span data-stu-id="1dae0-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="1dae0-111">Questo comando consente di ottenere informazioni su tutti i certificati di revoca client associati al gateway di rete virtuale denominato ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="1dae0-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="1dae0-112">Esempio 2: ottenere informazioni su specifici certificati di revoca del client</span><span class="sxs-lookup"><span data-stu-id="1dae0-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="1dae0-113">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="1dae0-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="1dae0-114">In questo caso, tuttavia, il parametro *VpnClientRevokedCertificateName* viene usato per limitare i dati restituiti a uno specifico certificato revocato dal client: il certificato con il nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="1dae0-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="1dae0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dae0-115">PARAMETERS</span></span>

### <span data-ttu-id="1dae0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dae0-116">-DefaultProfile</span></span>
<span data-ttu-id="1dae0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dae0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dae0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dae0-118">-ResourceGroupName</span></span>
<span data-ttu-id="1dae0-119">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1dae0-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="1dae0-120">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dae0-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1dae0-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1dae0-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1dae0-122">Specifica il nome del gateway di rete virtuale in cui sono assegnate le informazioni del certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="1dae0-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="1dae0-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="1dae0-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="1dae0-124">Specifica il nome del certificato del client VPN che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dae0-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dae0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dae0-125">CommonParameters</span></span>
<span data-ttu-id="1dae0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dae0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dae0-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dae0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dae0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dae0-128">INPUTS</span></span>

## <span data-ttu-id="1dae0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dae0-129">OUTPUTS</span></span>

###  
<span data-ttu-id="1dae0-130">**Get-AzureRmVpnClientRevokedCertificate** restituisce le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="1dae0-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="1dae0-131">Note</span><span class="sxs-lookup"><span data-stu-id="1dae0-131">NOTES</span></span>

## <span data-ttu-id="1dae0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dae0-132">RELATED LINKS</span></span>

[<span data-ttu-id="1dae0-133">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1dae0-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="1dae0-134">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1dae0-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="1dae0-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1dae0-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


