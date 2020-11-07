---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 516056afea32dde540bbac4cfcccf6eefc79143e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687152"
---
# <span data-ttu-id="157c4-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="157c4-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="157c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="157c4-102">SYNOPSIS</span></span>
<span data-ttu-id="157c4-103">Aggiunge un certificato radice del client VPN.</span><span class="sxs-lookup"><span data-stu-id="157c4-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="157c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="157c4-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="157c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="157c4-105">DESCRIPTION</span></span>
<span data-ttu-id="157c4-106">Il cmdlet **Add-AzureRmVpnClientRootCertificate** aggiunge un certificato radice a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="157c4-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="157c4-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice.</span><span class="sxs-lookup"><span data-stu-id="157c4-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="157c4-108">In base alla progettazione, tutti i certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="157c4-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="157c4-109">Questo cmdlet assegna un certificato esistente come certificato radice del gateway.</span><span class="sxs-lookup"><span data-stu-id="157c4-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="157c4-110">Se non si dispone di un certificato X. 509 disponibile, è possibile generarne uno tramite l'infrastruttura a chiave pubblica o utilizzare un generatore di certificati, ad esempio makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="157c4-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="157c4-111">Per aggiungere un certificato radice, devi specificare il nome del certificato e fornisci una rappresentazione testuale del certificato (Vedi *il parametro PublicCertData* per altre informazioni).</span><span class="sxs-lookup"><span data-stu-id="157c4-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="157c4-112">Azure consente di assegnare più di un certificato radice a un gateway.</span><span class="sxs-lookup"><span data-stu-id="157c4-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="157c4-113">Più certificati radice sono spesso distribuiti da organizzazioni che includono utenti di più di una società.</span><span class="sxs-lookup"><span data-stu-id="157c4-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="157c4-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="157c4-114">EXAMPLES</span></span>

### <span data-ttu-id="157c4-115">Esempio 1: aggiungere un certificato radice client a un gateway virtuale</span><span class="sxs-lookup"><span data-stu-id="157c4-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="157c4-116">Questo esempio aggiunge un certificato radice client a un gateway virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="157c4-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="157c4-117">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato radice e archivia i dati di testo la variabile denominata $text.</span><span class="sxs-lookup"><span data-stu-id="157c4-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="157c4-118">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima riga e dell'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="157c4-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="157c4-119">Il testo estratto viene archiviato in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="157c4-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="157c4-120">Il terzo comando usa quindi il testo archiviato in $CertificateText con il cmdlet **Add-AzureRmVpnClientRootCertificate** per aggiungere il certificato radice al gateway.</span><span class="sxs-lookup"><span data-stu-id="157c4-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="157c4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="157c4-121">PARAMETERS</span></span>

### <span data-ttu-id="157c4-122">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="157c4-122">-PublicCertData</span></span>
<span data-ttu-id="157c4-123">Specifica la rappresentazione testuale del certificato radice da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="157c4-123">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="157c4-124">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (usando la codifica Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="157c4-124">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="157c4-125">Quando si esegue questa operazione, verrà visualizzato l'output simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato qui):</span><span class="sxs-lookup"><span data-stu-id="157c4-125">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="157c4-126">-----INIZIARE il certificato-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----certificato finale-----</span><span class="sxs-lookup"><span data-stu-id="157c4-126">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="157c4-127">PublicCertData è costituito da tutte le linee tra la prima riga (-----iniziare il certificato-----) e l'ultima riga (----------certificato finale) nel file.</span><span class="sxs-lookup"><span data-stu-id="157c4-127">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="157c4-128">Puoi recuperare questi dati usando comandi di Windows PowerShell simili a questi: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="157c4-128">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="157c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="157c4-130">Specifica il nome del gruppo di risorse a cui è assegnato il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="157c4-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="157c4-131">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="157c4-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="157c4-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="157c4-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="157c4-133">Specifica il nome del gateway di rete virtuale in cui viene aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="157c4-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="157c4-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="157c4-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="157c4-135">Specifica il nome del certificato radice client aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="157c4-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="157c4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157c4-136">-DefaultProfile</span></span>
<span data-ttu-id="157c4-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="157c4-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="157c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157c4-138">CommonParameters</span></span>
<span data-ttu-id="157c4-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157c4-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157c4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157c4-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="157c4-141">INPUTS</span></span>

## <span data-ttu-id="157c4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="157c4-142">OUTPUTS</span></span>

### <span data-ttu-id="157c4-143">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="157c4-143">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="157c4-144">Note</span><span class="sxs-lookup"><span data-stu-id="157c4-144">NOTES</span></span>

## <span data-ttu-id="157c4-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="157c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="157c4-146">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="157c4-146">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="157c4-147">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="157c4-147">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="157c4-148">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="157c4-148">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)

