---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 861ea7bcfbfbe8a713934e2dc80a4448a2a98c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678047"
---
# <span data-ttu-id="d3d82-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d82-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d3d82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3d82-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d82-103">Rimuove un certificato di revoca del client VPN.</span><span class="sxs-lookup"><span data-stu-id="d3d82-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="d3d82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d82-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d82-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d82-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d82-106">Il cmdlet **Remove-AzVpnClientRevokedCertificate** rimuove un certificato di revoca del client da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3d82-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="d3d82-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d3d82-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="d3d82-108">Se si rimuovono i computer client di un certificato di revoca del client, è possibile usare il certificato precedentemente vietato per creare una connessione VPN (Virtual Private Network).</span><span class="sxs-lookup"><span data-stu-id="d3d82-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="d3d82-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d82-109">EXAMPLES</span></span>

### <span data-ttu-id="d3d82-110">Esempio 1: rimuovere un certificato di revoca del client da un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d3d82-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="d3d82-111">Questo comando rimuove un certificato di revoca client da un gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="d3d82-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="d3d82-112">Per rimuovere un certificato di revoca del client, è necessario specificare sia il nome del certificato che l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="d3d82-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="d3d82-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3d82-113">PARAMETERS</span></span>

### <span data-ttu-id="d3d82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d82-114">-DefaultProfile</span></span>
<span data-ttu-id="d3d82-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d82-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3d82-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d82-116">-ResourceGroupName</span></span>
<span data-ttu-id="d3d82-117">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3d82-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="d3d82-118">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d82-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="d3d82-119">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="d3d82-119">-Thumbprint</span></span>
<span data-ttu-id="d3d82-120">Specifica l'identificatore univoco del certificato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d3d82-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="d3d82-121">Puoi restituire informazioni sulle identificazioni personali per i certificati usando un comando di Windows PowerShell simile al seguente: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="d3d82-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="d3d82-122">Il comando precedente restituisce informazioni per tutti i certificati del computer locale presenti nell'archivio certificati radice.</span><span class="sxs-lookup"><span data-stu-id="d3d82-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="d3d82-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d3d82-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d3d82-124">Specifica il nome del gateway di rete virtuale a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="d3d82-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="d3d82-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="d3d82-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="d3d82-126">Specifica il nome del certificato client VPN da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d3d82-126">Specifies the name of the VPN client certificate being removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3d82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d82-127">CommonParameters</span></span>
<span data-ttu-id="d3d82-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d82-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d82-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d82-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3d82-130">INPUTS</span></span>

### <span data-ttu-id="d3d82-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3d82-131">System.String</span></span>

## <span data-ttu-id="d3d82-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d82-132">OUTPUTS</span></span>

### <span data-ttu-id="d3d82-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3d82-133">System.Boolean</span></span>

## <span data-ttu-id="d3d82-134">Note</span><span class="sxs-lookup"><span data-stu-id="d3d82-134">NOTES</span></span>

## <span data-ttu-id="d3d82-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d82-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3d82-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d82-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="d3d82-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d82-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="d3d82-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3d82-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


