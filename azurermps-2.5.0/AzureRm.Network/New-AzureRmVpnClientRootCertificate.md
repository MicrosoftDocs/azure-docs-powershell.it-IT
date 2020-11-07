---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: a5f562fd05432abc502d648ca7fae614744e4f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866869"
---
# <span data-ttu-id="00001-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="00001-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="00001-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00001-102">SYNOPSIS</span></span>
<span data-ttu-id="00001-103">Crea un nuovo certificato radice del client VPN.</span><span class="sxs-lookup"><span data-stu-id="00001-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00001-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00001-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00001-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00001-105">DESCRIPTION</span></span>
<span data-ttu-id="00001-106">Il cmdlet **New-AzureRmVpnClientRootCertificate** crea un nuovo certificato radice VPN da usare in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="00001-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="00001-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="00001-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="00001-108">Questo cmdlet crea un certificato autonomo che non è assegnato a un gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="00001-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="00001-109">Il certificato creato da **New-AzureRmVpnClientRootCertificate** viene invece usato insieme al cmdlet New-AzureRmVirtualNetworkGateway quando si crea un nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="00001-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="00001-110">Supponiamo ad esempio di creare un nuovo certificato e archiviarlo in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="00001-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="00001-111">Puoi quindi usare l'oggetto certificato durante la creazione di un nuovo gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="00001-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="00001-112">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="00001-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="00001-113">Per altre informazioni, vedere la documentazione relativa al cmdlet New-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="00001-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="00001-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00001-114">EXAMPLES</span></span>

### <span data-ttu-id="00001-115">Esempio 1: creare un certificato radice di AClient</span><span class="sxs-lookup"><span data-stu-id="00001-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="00001-116">Questo esempio crea un certificato radice client e archivia l'oggetto Certificate in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="00001-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="00001-117">Questa variabile può quindi essere usata dal cmdlet **New-AzureRmVirtualNetworkGateway** per aggiungere un certificato radice a un nuovo gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="00001-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="00001-118">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione di testo esportata in precedenza del certificato radice; i dati di testo vengono archiviati in una variabile denominata $Text.</span><span class="sxs-lookup"><span data-stu-id="00001-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="00001-119">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima riga e dell'ultima riga, archiviando il testo estratto in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="00001-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="00001-120">Il terzo comando usa il cmdlet **New-AzureRmVpnClientRootCertificate** per creare il certificato, archiviando l'oggetto creato in una variabile denominata $certificate.</span><span class="sxs-lookup"><span data-stu-id="00001-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="00001-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00001-121">PARAMETERS</span></span>

### <span data-ttu-id="00001-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00001-122">-DefaultProfile</span></span>
<span data-ttu-id="00001-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00001-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00001-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="00001-124">-Name</span></span>
<span data-ttu-id="00001-125">Specifica un nome per il nuovo certificato radice client.</span><span class="sxs-lookup"><span data-stu-id="00001-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="00001-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="00001-126">-PublicCertData</span></span>
<span data-ttu-id="00001-127">Specifica una rappresentazione testuale del certificato radice da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="00001-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="00001-128">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (usando la codifica Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="00001-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="00001-129">Dovrebbe essere visualizzato l'output simile a questo (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato qui):</span><span class="sxs-lookup"><span data-stu-id="00001-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="00001-130">-----INIZIARE il certificato-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----certificato finale-----</span><span class="sxs-lookup"><span data-stu-id="00001-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="00001-131">PublicCertData è costituito da tutte le linee tra la prima riga (-----iniziare il certificato-----) e l'ultima riga (----------certificato finale) nel file.</span><span class="sxs-lookup"><span data-stu-id="00001-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="00001-132">Puoi recuperare PublicCertData usando i comandi di Windows PowerShell in modo simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="00001-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="00001-133">$Text = Get-Content-path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="00001-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="00001-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00001-134">CommonParameters</span></span>
<span data-ttu-id="00001-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00001-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00001-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00001-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00001-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00001-137">INPUTS</span></span>

###  
<span data-ttu-id="00001-138">Questo cmdlet non accetta l'input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="00001-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="00001-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00001-139">OUTPUTS</span></span>

###  
<span data-ttu-id="00001-140">Questo cmdlet crea nuove istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="00001-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="00001-141">Note</span><span class="sxs-lookup"><span data-stu-id="00001-141">NOTES</span></span>

## <span data-ttu-id="00001-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00001-142">RELATED LINKS</span></span>

[<span data-ttu-id="00001-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="00001-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="00001-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="00001-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="00001-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="00001-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


