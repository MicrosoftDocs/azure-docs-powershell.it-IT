---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8f1c81dbfb3d8c42b359464ce33a0053fdc25143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687902"
---
# <span data-ttu-id="c20b0-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c20b0-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c20b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c20b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c20b0-103">Aggiunge un certificato di revoca client VPN.</span><span class="sxs-lookup"><span data-stu-id="c20b0-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c20b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c20b0-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c20b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c20b0-106">Il cmdlet **Add-AzureRmVpnClientRevokedCertificate** assegna un certificato di revoca client a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c20b0-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="c20b0-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c20b0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="c20b0-108">Per usare questo cmdlet, è necessario specificare sia il nome del certificato che l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="c20b0-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="c20b0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c20b0-109">EXAMPLES</span></span>

### <span data-ttu-id="c20b0-110">Esempio 1: aggiungere un nuovo certificato di revoca client a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c20b0-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c20b0-111">Questo comando aggiunge un nuovo certificato di revoca client al gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="c20b0-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="c20b0-112">Per aggiungere il certificato, è necessario specificare sia il nome del certificato che l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="c20b0-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="c20b0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c20b0-113">PARAMETERS</span></span>

### <span data-ttu-id="c20b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20b0-114">-DefaultProfile</span></span>
<span data-ttu-id="c20b0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c20b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c20b0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c20b0-116">-ResourceGroupName</span></span>
<span data-ttu-id="c20b0-117">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c20b0-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="c20b0-118">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20b0-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="c20b0-119">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="c20b0-119">-Thumbprint</span></span>
<span data-ttu-id="c20b0-120">Specifica l'identificatore univoco del certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="c20b0-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="c20b0-121">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="c20b0-121">For example:</span></span>

<span data-ttu-id="c20b0-122">-Identificazione personale "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="c20b0-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="c20b0-123">È possibile ottenere informazioni sulle identificazioni personali per i certificati usando un comando di Windows PowerShell simile al seguente: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="c20b0-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="c20b0-124">Il comando precedente consente di ottenere informazioni per tutti i certificati del computer locale presenti nell'archivio certificati radice.</span><span class="sxs-lookup"><span data-stu-id="c20b0-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20b0-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c20b0-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c20b0-126">Specifica il nome del gateway di rete virtuale in cui deve essere aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="c20b0-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="c20b0-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="c20b0-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="c20b0-128">Specifica il nome del certificato client VPN da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="c20b0-128">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20b0-129">CommonParameters</span></span>
<span data-ttu-id="c20b0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c20b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20b0-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20b0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20b0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c20b0-132">INPUTS</span></span>

### <span data-ttu-id="c20b0-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c20b0-133">None</span></span>
<span data-ttu-id="c20b0-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c20b0-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c20b0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c20b0-135">OUTPUTS</span></span>

### <span data-ttu-id="c20b0-136">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c20b0-136">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c20b0-137">Note</span><span class="sxs-lookup"><span data-stu-id="c20b0-137">NOTES</span></span>

## <span data-ttu-id="c20b0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c20b0-138">RELATED LINKS</span></span>

[<span data-ttu-id="c20b0-139">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c20b0-139">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c20b0-140">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c20b0-140">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c20b0-141">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c20b0-141">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


