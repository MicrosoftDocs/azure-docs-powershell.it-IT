---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510468"
---
# <span data-ttu-id="c1279-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c1279-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c1279-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1279-102">SYNOPSIS</span></span>
<span data-ttu-id="c1279-103">Crea un nuovo client VPN-certificato di revoca.</span><span class="sxs-lookup"><span data-stu-id="c1279-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1279-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1279-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1279-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1279-105">DESCRIPTION</span></span>
<span data-ttu-id="c1279-106">Il cmdlet **New-AzureRmVpnClientRevokedCertificate** crea un nuovo client di rete privata virtuale (VPN)-certificato di revoca per l'uso in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1279-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="c1279-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c1279-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="c1279-108">Questo cmdlet crea un certificato autonomo che non è assegnato a un gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1279-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="c1279-109">Il certificato creato da **New-AzureRmVpnClientRevokedCertificate** viene invece usato insieme al cmdlet New-AzureRmVirtualNetworkGateway quando crea un nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="c1279-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="c1279-110">Supponiamo, ad esempio, di creare un nuovo certificato e archiviarlo in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="c1279-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="c1279-111">Puoi quindi usare l'oggetto certificato quando crei un nuovo gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1279-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="c1279-112">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="c1279-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="c1279-113">Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c1279-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="c1279-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1279-114">EXAMPLES</span></span>

### <span data-ttu-id="c1279-115">Esempio 1: creare un nuovo certificato revocato dal client</span><span class="sxs-lookup"><span data-stu-id="c1279-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c1279-116">Questo comando crea un nuovo certificato revocato dal client e archivia l'oggetto certificato in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="c1279-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="c1279-117">Questa variabile può quindi essere usata dal cmdlet **New-AzureRmVirtualNetworkGateway** per aggiungere il certificato a un nuovo gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1279-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="c1279-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1279-118">PARAMETERS</span></span>

### <span data-ttu-id="c1279-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1279-119">-Name</span></span>
<span data-ttu-id="c1279-120">Specifica un nome univoco per il nuovo certificato di revoca del client.</span><span class="sxs-lookup"><span data-stu-id="c1279-120">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1279-121">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="c1279-121">-Thumbprint</span></span>
<span data-ttu-id="c1279-122">Specifica l'identificatore univoco del certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="c1279-122">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="c1279-123">Puoi restituire informazioni sulle identificazioni personali per i certificati usando un comando di Windows PowerShell simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="c1279-123">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="c1279-124">Il comando precedente restituisce informazioni per tutti i certificati del computer locale presenti nell'archivio certificati radice.</span><span class="sxs-lookup"><span data-stu-id="c1279-124">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1279-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1279-125">-DefaultProfile</span></span>
<span data-ttu-id="c1279-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1279-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1279-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1279-127">CommonParameters</span></span>
<span data-ttu-id="c1279-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1279-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1279-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1279-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1279-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1279-130">INPUTS</span></span>

###  
<span data-ttu-id="c1279-131">Questo cmdlet non accetta l'input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1279-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="c1279-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1279-132">OUTPUTS</span></span>

###  
<span data-ttu-id="c1279-133">Questo cmdlet crea nuove istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="c1279-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="c1279-134">Note</span><span class="sxs-lookup"><span data-stu-id="c1279-134">NOTES</span></span>

## <span data-ttu-id="c1279-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1279-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1279-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c1279-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c1279-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c1279-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c1279-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c1279-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)

