---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207003"
---
# <span data-ttu-id="4f62c-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f62c-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="4f62c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f62c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f62c-103">Aggiunge un certificato radice del client VPN.</span><span class="sxs-lookup"><span data-stu-id="4f62c-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="4f62c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f62c-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f62c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f62c-105">DESCRIPTION</span></span>
<span data-ttu-id="4f62c-106">Il cmdlet **Add-AzVpnClientRootCertificate aggiunge** un certificato radice a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4f62c-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="4f62c-107">I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice.</span><span class="sxs-lookup"><span data-stu-id="4f62c-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="4f62c-108">Per impostazione predefinita, tutti i certificati usati nel gateway considera attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="4f62c-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="4f62c-109">Questo cmdlet assegna un certificato esistente come certificato radice del gateway.</span><span class="sxs-lookup"><span data-stu-id="4f62c-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="4f62c-110">Se non è disponibile un certificato X.509, è possibile generarne uno tramite l'infrastruttura della chiave pubblica oppure usare un generatore di certificati, ad esempio makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="4f62c-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="4f62c-111">Per aggiungere un certificato radice, è necessario specificare il nome del certificato e fornire una rappresentazione solo testuale del certificato (per altre informazioni, vedere il parametro *PublicCertData).*</span><span class="sxs-lookup"><span data-stu-id="4f62c-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="4f62c-112">Azure consente di assegnare più certificati radice a un gateway.</span><span class="sxs-lookup"><span data-stu-id="4f62c-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="4f62c-113">Più certificati radice vengono spesso distribuiti da organizzazioni che includono utenti di più aziende.</span><span class="sxs-lookup"><span data-stu-id="4f62c-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="4f62c-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f62c-114">EXAMPLES</span></span>

### <span data-ttu-id="4f62c-115">Esempio 1: Aggiungere un certificato radice client a un gateway virtuale</span><span class="sxs-lookup"><span data-stu-id="4f62c-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="4f62c-116">Questo esempio aggiunge un certificato radice client a un gateway virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4f62c-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="4f62c-117">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione di testo esportata in precedenza del certificato radice e archivia i dati di testo la variabile denominata $Text.</span><span class="sxs-lookup"><span data-stu-id="4f62c-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="4f62c-118">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo ad eccezione della prima e dell'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="4f62c-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="4f62c-119">Il testo estratto viene archiviato in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="4f62c-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="4f62c-120">Il terzo comando usa quindi il testo archiviato in $CertificateText con il cmdlet **Add-AzVpnClientRootCertificate** per aggiungere il certificato radice al gateway.</span><span class="sxs-lookup"><span data-stu-id="4f62c-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="4f62c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f62c-121">PARAMETERS</span></span>

### <span data-ttu-id="4f62c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f62c-122">-DefaultProfile</span></span>
<span data-ttu-id="4f62c-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f62c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f62c-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="4f62c-124">-PublicCertData</span></span>
<span data-ttu-id="4f62c-125">Specifica la rappresentazione testuale del certificato radice da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4f62c-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="4f62c-126">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (con codifica Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="4f62c-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="4f62c-127">In questo caso, l'output sarà simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato di seguito): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData è costituito da tutte le righe tra la prima riga (----- BEGIN CERTIFICATE -----) e l'ultima riga (----- END CERTIFICATE -----) del file.</span><span class="sxs-lookup"><span data-stu-id="4f62c-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="4f62c-128">È possibile recuperare questi dati usando Windows PowerShell comandi simili ai seguenti: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="4f62c-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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

### <span data-ttu-id="4f62c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f62c-129">-ResourceGroupName</span></span>
<span data-ttu-id="4f62c-130">Specifica il nome del gruppo di risorse a cui è assegnato il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="4f62c-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="4f62c-131">I gruppi di risorse categorizzano gli articoli per semplificare la gestione dell'inventario e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f62c-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="4f62c-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4f62c-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4f62c-133">Specifica il nome del gateway di rete virtuale in cui viene aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="4f62c-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="4f62c-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="4f62c-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="4f62c-135">Specifica il nome del certificato radice client aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f62c-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4f62c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f62c-136">CommonParameters</span></span>
<span data-ttu-id="4f62c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f62c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f62c-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f62c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f62c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f62c-139">INPUTS</span></span>

### <span data-ttu-id="4f62c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4f62c-140">System.String</span></span>

## <span data-ttu-id="4f62c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f62c-141">OUTPUTS</span></span>

### <span data-ttu-id="4f62c-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f62c-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="4f62c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f62c-143">NOTES</span></span>

## <span data-ttu-id="4f62c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f62c-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f62c-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f62c-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4f62c-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f62c-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4f62c-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f62c-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


