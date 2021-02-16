---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191831"
---
# <span data-ttu-id="06abc-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="06abc-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="06abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06abc-102">SYNOPSIS</span></span>
<span data-ttu-id="06abc-103">Crea un nuovo certificato radice del client VPN.</span><span class="sxs-lookup"><span data-stu-id="06abc-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="06abc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06abc-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06abc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06abc-105">DESCRIPTION</span></span>
<span data-ttu-id="06abc-106">Il cmdlet **New-AzVpnClientRootCertificate** crea un nuovo certificato radice VPN da usare in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="06abc-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="06abc-107">I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice: tutti gli altri certificati usati nel gateway considera attendibili il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="06abc-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="06abc-108">Questo cmdlet crea un certificato autonomo non assegnato a un gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="06abc-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="06abc-109">Il certificato creato da **New-AzVpnClientRootCertificate** viene usato in combinazione con il cmdlet New-AzVirtualNetworkGateway durante la creazione di un nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="06abc-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="06abc-110">Si supponga, ad esempio, di creare un nuovo certificato e di archiviarlo in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="06abc-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="06abc-111">È quindi possibile usare tale oggetto certificato durante la creazione di un nuovo gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="06abc-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="06abc-112">Ad esempio, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="06abc-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="06abc-113">Per altre informazioni, vedere la documentazione del cmdlet New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="06abc-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="06abc-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06abc-114">EXAMPLES</span></span>

### <span data-ttu-id="06abc-115">Esempio 1: Creare un certificato radice client</span><span class="sxs-lookup"><span data-stu-id="06abc-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="06abc-116">Questo esempio crea un certificato radice client e archivia l'oggetto certificato in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="06abc-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="06abc-117">Questa variabile può quindi essere usata dal cmdlet **New-AzVirtualNetworkGateway** per aggiungere un certificato radice a un nuovo gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="06abc-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="06abc-118">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato radice; che i dati di testo vengono archiviati in una variabile denominata $Text.</span><span class="sxs-lookup"><span data-stu-id="06abc-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="06abc-119">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima e dell'ultima riga, archiviando il testo estratto in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="06abc-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="06abc-120">Il terzo comando usa il cmdlet **New-AzVpnClientRootCertificate** per creare il certificato, archiviando l'oggetto creato in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="06abc-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="06abc-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06abc-121">PARAMETERS</span></span>

### <span data-ttu-id="06abc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06abc-122">-DefaultProfile</span></span>
<span data-ttu-id="06abc-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06abc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06abc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="06abc-124">-Name</span></span>
<span data-ttu-id="06abc-125">Specifica un nome per il nuovo certificato radice client.</span><span class="sxs-lookup"><span data-stu-id="06abc-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="06abc-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="06abc-126">-PublicCertData</span></span>
<span data-ttu-id="06abc-127">Specifica una rappresentazione testuale del certificato radice da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="06abc-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="06abc-128">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (con codifica Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="06abc-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="06abc-129">L'output dovrebbe essere simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato di seguito): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData è costituito da tutte le righe tra la prima riga (----- BEGIN CERTIFICATE -----) e l'ultima riga (----- END CERTIFICATE -----) nel file.</span><span class="sxs-lookup"><span data-stu-id="06abc-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="06abc-130">È possibile recuperare PublicCertData usando comandi di Windows PowerShell simili ai seguenti: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="06abc-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="06abc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06abc-131">CommonParameters</span></span>
<span data-ttu-id="06abc-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06abc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06abc-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06abc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06abc-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="06abc-134">INPUTS</span></span>

### <span data-ttu-id="06abc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="06abc-135">System.String</span></span>

## <span data-ttu-id="06abc-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06abc-136">OUTPUTS</span></span>

### <span data-ttu-id="06abc-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="06abc-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="06abc-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="06abc-138">NOTES</span></span>

## <span data-ttu-id="06abc-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06abc-139">RELATED LINKS</span></span>

[<span data-ttu-id="06abc-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="06abc-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="06abc-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="06abc-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="06abc-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="06abc-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


