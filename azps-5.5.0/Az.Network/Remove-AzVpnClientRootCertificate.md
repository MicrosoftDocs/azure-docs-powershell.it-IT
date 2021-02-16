---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179406"
---
# <span data-ttu-id="6677b-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6677b-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="6677b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6677b-102">SYNOPSIS</span></span>
<span data-ttu-id="6677b-103">Rimuove un certificato radice del client VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="6677b-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="6677b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6677b-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6677b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6677b-105">DESCRIPTION</span></span>
<span data-ttu-id="6677b-106">Il cmdlet **Remove-AzVpnClientRootCertificate rimuove** il certificato radice specificato da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6677b-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="6677b-107">I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice: tutti gli altri certificati usati nel gateway considera attendibili il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="6677b-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="6677b-108">Se si rimuove un certificato radice che usa il certificato a scopo di autenticazione, non sarà più possibile connettersi al gateway.</span><span class="sxs-lookup"><span data-stu-id="6677b-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="6677b-109">Quando si usa **Remove-AzVpnClientRootCertificate,** è necessario specificare sia il nome del certificato che una rappresentazione testuale dei dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="6677b-109">When you use **Remove-AzVpnClientRootCertificate**, you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="6677b-110">Per altre informazioni sulla rappresentazione testuale di un certificato, vedere la *descrizione del parametro PublicCertData.*</span><span class="sxs-lookup"><span data-stu-id="6677b-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="6677b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6677b-111">EXAMPLES</span></span>

### <span data-ttu-id="6677b-112">Esempio 1: Rimuovere un certificato radice client da un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="6677b-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="6677b-113">Questo esempio rimuove un certificato radice client denominato ContosoRootCertificate dal gateway di rete virtuale ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="6677b-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="6677b-114">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato; questa rappresentazione di testo è archiviata in una variabile $Text.</span><span class="sxs-lookup"><span data-stu-id="6677b-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="6677b-115">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo in $Text ad eccezione della prima e dell'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="6677b-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="6677b-116">Questo testo estratto viene archiviato in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="6677b-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="6677b-117">Il terzo comando usa le informazioni archiviate nella variabile $CertificateText insieme al cmdlet **Remove-AzVpnClientRootCertificate** per rimuovere il certificato dal gateway.</span><span class="sxs-lookup"><span data-stu-id="6677b-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="6677b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6677b-118">PARAMETERS</span></span>

### <span data-ttu-id="6677b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6677b-119">-DefaultProfile</span></span>
<span data-ttu-id="6677b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6677b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6677b-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="6677b-121">-PublicCertData</span></span>
<span data-ttu-id="6677b-122">Specifica la rappresentazione testuale del certificato radice da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6677b-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="6677b-123">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (con codifica Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="6677b-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="6677b-124">L'output dovrebbe essere simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato di seguito): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData è costituito da tutte le righe tra la prima riga (----- BEGIN CERTIFICATE -----) e l'ultima riga (----- END CERTIFICATE -----) nel file.</span><span class="sxs-lookup"><span data-stu-id="6677b-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="6677b-125">È possibile recuperare PublicCertData usando comandi di Windows PowerShell simili ai seguenti: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="6677b-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="6677b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6677b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6677b-127">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6677b-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="6677b-128">I gruppi di risorse categorizzano gli articoli per semplificare la gestione dell'inventario e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6677b-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="6677b-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6677b-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6677b-130">Specifica il nome del gateway di rete virtuale da cui viene rimosso il certificato.</span><span class="sxs-lookup"><span data-stu-id="6677b-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="6677b-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="6677b-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="6677b-132">Specifica il nome del certificato radice client rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6677b-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6677b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6677b-133">CommonParameters</span></span>
<span data-ttu-id="6677b-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6677b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6677b-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6677b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6677b-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="6677b-136">INPUTS</span></span>

### <span data-ttu-id="6677b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6677b-137">System.String</span></span>

## <span data-ttu-id="6677b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6677b-138">OUTPUTS</span></span>

### <span data-ttu-id="6677b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6677b-139">System.Boolean</span></span>

## <span data-ttu-id="6677b-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="6677b-140">NOTES</span></span>

## <span data-ttu-id="6677b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6677b-141">RELATED LINKS</span></span>

[<span data-ttu-id="6677b-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6677b-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="6677b-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6677b-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="6677b-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6677b-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


