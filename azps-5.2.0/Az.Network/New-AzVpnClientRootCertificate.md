---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336580"
---
# <span data-ttu-id="8a5e8-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a5e8-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="8a5e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5e8-103">Crea un nuovo certificato radice del client VPN.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="8a5e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a5e8-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a5e8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="8a5e8-106">Il cmdlet **New-AzVpnClientRootCertificate** crea un nuovo certificato radice VPN da usare in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="8a5e8-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="8a5e8-108">Questo cmdlet crea un certificato autonomo che non è assegnato a un gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="8a5e8-109">Il certificato creato da **New-AzVpnClientRootCertificate** viene invece usato insieme al cmdlet New-AzVirtualNetworkGateway quando si crea un nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="8a5e8-110">Supponiamo ad esempio di creare un nuovo certificato e archiviarlo in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="8a5e8-111">Puoi quindi usare l'oggetto certificato durante la creazione di un nuovo gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="8a5e8-112">Ad esempio, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="8a5e8-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="8a5e8-113">Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="8a5e8-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a5e8-114">EXAMPLES</span></span>

### <span data-ttu-id="8a5e8-115">Esempio 1: creare un certificato radice client</span><span class="sxs-lookup"><span data-stu-id="8a5e8-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="8a5e8-116">Questo esempio crea un certificato radice client e archivia l'oggetto Certificate in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="8a5e8-117">Questa variabile può quindi essere usata dal cmdlet **New-AzVirtualNetworkGateway** per aggiungere un certificato radice a un nuovo gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="8a5e8-118">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione di testo esportata in precedenza del certificato radice; i dati di testo vengono archiviati in una variabile denominata $Text.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="8a5e8-119">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima riga e dell'ultima riga, archiviando il testo estratto in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="8a5e8-120">Il terzo comando usa il cmdlet **New-AzVpnClientRootCertificate** per creare il certificato, archiviando l'oggetto creato in una variabile denominata $certificate.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="8a5e8-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a5e8-121">PARAMETERS</span></span>

### <span data-ttu-id="8a5e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5e8-122">-DefaultProfile</span></span>
<span data-ttu-id="8a5e8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a5e8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a5e8-124">-Name</span></span>
<span data-ttu-id="8a5e8-125">Specifica un nome per il nuovo certificato radice client.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="8a5e8-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="8a5e8-126">-PublicCertData</span></span>
<span data-ttu-id="8a5e8-127">Specifica una rappresentazione testuale del certificato radice da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="8a5e8-128">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (usando la codifica Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="8a5e8-129">Dovrebbe essere visualizzato l'output simile a questo (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato qui):-----iniziare il certificato-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----certificato finale-----PublicCertData è costituito da tutte le linee tra la prima riga (-----iniziare il certificato-----) e l'ultima riga (-----certificato di fine-----) nel file.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="8a5e8-130">Puoi recuperare PublicCertData usando i comandi di Windows PowerShell in modo simile al seguente: $Text = Get-Content-path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="8a5e8-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="8a5e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5e8-131">CommonParameters</span></span>
<span data-ttu-id="8a5e8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5e8-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a5e8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5e8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a5e8-134">INPUTS</span></span>

### <span data-ttu-id="8a5e8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8a5e8-135">System.String</span></span>

## <span data-ttu-id="8a5e8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a5e8-136">OUTPUTS</span></span>

### <span data-ttu-id="8a5e8-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a5e8-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="8a5e8-138">Note</span><span class="sxs-lookup"><span data-stu-id="8a5e8-138">NOTES</span></span>

## <span data-ttu-id="8a5e8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a5e8-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a5e8-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a5e8-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="8a5e8-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a5e8-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="8a5e8-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a5e8-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


